---
title: money_put 类 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: reference
f1_keywords:
- xlocmon/std::money_put
- xlocmon/std::money_put::char_type
- xlocmon/std::money_put::iter_type
- xlocmon/std::money_put::string_type
- xlocmon/std::money_put::do_put
- xlocmon/std::money_put::put
dev_langs:
- C++
helpviewer_keywords:
- std::money_put [C++]
- std::money_put [C++], char_type
- std::money_put [C++], iter_type
- std::money_put [C++], string_type
- std::money_put [C++], do_put
- std::money_put [C++], put
ms.assetid: f439fd56-c9b1-414c-95e1-66c918c6eee6
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 299d11ea29afa5331ef79c7947ccd2684713b29e
ms.sourcegitcommit: 761c5f7c506915f5a62ef3847714f43e9b815352
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2018
ms.locfileid: "44108897"
---
# <a name="moneyput-class"></a>money_put 类

此模板类描述一个对象来充当区域设置 facet，以便控制货币值向 `CharType` 类型序列的转换。

## <a name="syntax"></a>语法

```cpp
template <class CharType,
    class OutputIterator = ostreambuf_iterator<CharType>>
class money_put : public locale::facet;
```

### <a name="parameters"></a>参数

*CharType*<br/>
在程序中用于对区域设置中的字符进行编码的类型。

*OutputIterator*<br/>
供货币放置函数写入其输出结果的迭代器类型。

## <a name="remarks"></a>备注

对于任何区域设置 facet，静态对象 ID 的初始存储值为零。 首次尝试访问其存储值后，将在 **ID** 中存储唯一正值。

### <a name="constructors"></a>构造函数

|构造函数|描述|
|-|-|
|[money_put](#money_put)|`money_put` 类型的对象的构造函数。|

### <a name="typedefs"></a>Typedef

|类型名称|描述|
|-|-|
|[char_type](#char_type)|一种类型，此类型用于描述区域设置使用的字符。|
|[iter_type](#iter_type)|一种类型，此类型描述输出迭代器。|
|[string_type](#string_type)|一种类型，此类型描述包含 `CharType` 类型字符的字符串。|

### <a name="member-functions"></a>成员函数

|成员函数|描述|
|-|-|
|[do_put](#do_put)|一种虚拟函数，通过调用此函数可将数字或字符串转换为表示货币值的字符序列。|
|[put](#put)|将数字或字符串转换为表示货币值的字符序列。|

## <a name="requirements"></a>要求

**标头：** \<locale>

**命名空间：** std

## <a name="char_type"></a>  money_put::char_type

一种类型，此类型用于描述区域设置使用的字符。

```cpp
typedef CharType char_type;
```

### <a name="remarks"></a>备注

该类型是模板参数 **CharType** 的同义词。

## <a name="do_put"></a>  money_put::do_put

一种虚拟函数，通过调用此函数可将数字或字符串转换为表示货币值的字符序列。

```cpp
virtual iter_type do_put(
    iter_type next,
    bool _Intl,
    ios_base& _Iosbase,
    CharType _Fill,
    const string_type& val) const;


virtual iter_type do_put(
    iter_type next,
    bool _Intl,
    ios_base& _Iosbase,
    CharType _Fill,
    long double val) const;
```

### <a name="parameters"></a>参数

*next*<br/>
发现插入的字符串中第一个元素的迭代器。

*_Intl*<br/>
一个布尔值，该值指示在序列中预期的货币符号的类型：如果为国际，则为 **true**，如果为国内，则为 **false**。

*_Iosbase*<br/>
一种格式标志，设定时表示货币符号是可选项；否则，它是必需项

*_Fill*<br/>
用于调整间距的字符。

*val*<br/>
要转换的字符串对象。

### <a name="return-value"></a>返回值

发现超出生成的最后一个元素的位置的输出迭代器。

### <a name="remarks"></a>备注

第一个受保护的虚拟成员函数生成有序元素*下一步*生成货币输出字段从[string_type](#string_type)对象*val*。 控制的序列*val*必须以与一个或多个十进制数字，可以后跟减号 （-），以表示数额。 该函数返回一个迭代器，指定超出生成货币输出字段的第一个元素。

第二个受保护的虚拟成员函数的行为与第一个相同只不过它实际上首先将*val*到序列中的十进制数，可以后跟一个减号，然后将转换该序列作为更高版本。

货币输出字段的格式由[区域设置 facet](../standard-library/locale-class.md#facet_class) fac 决定，而后者又由（有效）调用 [use_facet](../standard-library/locale-functions.md#use_facet) < [moneypunct](../standard-library/moneypunct-class.md)\< **CharType**, **intl**> >( **iosbase**. [getloc](../standard-library/ios-base-class.md#getloc)) 返回。

尤其是在下列情况下：

- **fac**. [pos_format](../standard-library/moneypunct-class.md#pos_format) 确定生成非负数值的字段组件所采用的顺序。

- **fac**. [neg_format](../standard-library/moneypunct-class.md#neg_format) 确定生成负数值的字段组件所采用的顺序。

- **fac**. [curr_symbol](../standard-library/moneypunct-class.md#curr_symbol) 确定要生成的货币符号的元素序列。

- **fac**. [positive_sign](../standard-library/moneypunct-class.md#positive_sign) 确定要生成的正号的元素序列。

- **fac**. [negative_sign](../standard-library/moneypunct-class.md#negative_sign) 确定要生成的负号的元素序列。

- **fac**. [grouping](../standard-library/moneypunct-class.md#grouping) 确定如何对任何小数点左侧的数字进行分组。

- **fac**. [thousands_sep](../standard-library/moneypunct-class.md#thousands_sep) 确定将任何小数点左侧的数字进行分组的元素。

- **fac**. [decimal_point](../standard-library/moneypunct-class.md#decimal_point) 确定从任何小数位分隔整数位的元素。

- **fac**. [frac_digits](../standard-library/moneypunct-class.md#frac_digits) 确定任何小数点右侧的有效位数。

如果符号字符串（**fac**. `negative_sign` 或 **fac**. `positive_sign`具有多个元素，则第一个元素会在等于 **money_base::sign** 的元素在 ( **fac**. `neg_format` 或 **fac**. `pos_format`）格式模式中出现的位置生成。 剩余所有元素在货币输出字段的末尾生成。

如果 **iosbase**. [flags](../standard-library/ios-base-class.md#flags) & [showbase](../standard-library/ios-functions.md#showbase) 不为零，则字符串 **fac**. `curr_symbol` 将在等于 **money_base::symbol** 的元素在此格式模式中出现的位置处生成。 否则，将不生成货币符号。

如果 **fac**. **grouping** 未采用任何分组约束（其首个元素具有值 CHAR_MAX），则 **fac**. `thousands_sep` 的任何实例都不会在货币输出字段的值部分（等于 **money_base::value** 的元素在格式模式中出现的位置）生成。 如果 **fac**. `frac_digits` 为零，则在十进制数字后不会生成 **fac**. `decimal_point` 的任何实例。 否则，生成的货币输出字段会将低位 **fac**. `frac_digits` 十进制数字置于小数点右侧。

对于任何数字输出字段，都会发生填充，除非 **iosbase**. **flags** & **iosbase**. [internal](../standard-library/ios-functions.md#internal) 不为零；将在等于 **money_base::space** 的元素在此格式模式中出现的位置处生成任何内部填充（如果确实出现该元素）。 否则，将在生成的序列之前出现内部填充。 填充字符为 **fill**。

该函数将调用 **iosbase**. **width**(0) 以便将字段宽度重置为零。

### <a name="example"></a>示例

请参阅 [put](#put) 的示例，其中虚拟成员函数由 **put** 调用。

## <a name="iter_type"></a>  money_put::iter_type

一种类型，此类型描述输出迭代器。

```cpp
typedef OutputIterator iter_type;
```

### <a name="remarks"></a>备注

该类型是模板参数 **OutputIterator** 的同义词。

## <a name="money_put"></a>  money_put::money_put

`money_put` 类型的对象的构造函数。

```cpp
explicit money_put(size_t _Refs = 0);
```

### <a name="parameters"></a>参数

*_Refs*<br/>
用于指定对象的内存管理类型的整数值。

### <a name="remarks"></a>备注

可能的值 *_Refs*参数和其重要性：

- 0：对象的生存期由包含该对象的区域设置管理。

- 1：必须手动管理对象的生存期。

- \> 1： 未定义这些值。

由于该析构函数受到保护，可能没有直接的示例。

构造函数通过 **locale::**[facet](../standard-library/locale-class.md#facet_class)( `_Refs`) 初始化其基对象。

## <a name="put"></a>  money_put::put

将数字或字符串转换为表示货币值的字符序列。

```cpp
iter_type put(
    iter_type next,
    bool _Intl,
    ios_base& _Iosbase,
    CharType _Fill,
    const string_type& val) const;


iter_type put(
    iter_type next,
    bool _Intl,
    ios_base& _Iosbase,
    CharType _Fill,
    long double val) const;
```

### <a name="parameters"></a>参数

*next*<br/>
发现插入的字符串中第一个元素的迭代器。

*_Intl*<br/>
一个布尔值，该值指示在序列中预期的货币符号的类型：如果为国际，则为 **true**，如果为国内，则为 **false**。

*_Iosbase*<br/>
一种格式标志，设定时表示货币符号是可选项；否则，它是必需项

*_Fill*<br/>
用于调整间距的字符。

*val*<br/>
要转换的字符串对象。

### <a name="return-value"></a>返回值

发现超出生成的最后一个元素的位置的输出迭代器。

### <a name="remarks"></a>备注

两个成员函数都返回 [do_put](#do_put)( `next`, `_Intl`, `_Iosbase`, `_Fill`, `val`)。

### <a name="example"></a>示例

```cpp
// money_put_put.cpp
// compile with: /EHsc
#include <locale>
#include <iostream>
#include <sstream>
using namespace std;
int main( )
{
//   locale loc( "german_germany" );
   locale loc( "english_canada" );
   basic_stringstream<char> psz, psz2;
   ios_base::iostate st = 0;

   psz2.imbue( loc );
   psz2.flags( psz2.flags( )|ios_base::showbase ); // force the printing of the currency symbol
   use_facet < money_put < char > >(loc).put(basic_ostream<char>::_Iter( psz2.rdbuf( ) ), true, psz2, st, 100012);
   if (st & ios_base::failbit)
      cout << "money_put( ) FAILED" << endl;
   else
      cout << "money_put( ) = \"" << psz2.rdbuf( )->str( ) <<"\""<< endl;

   st = 0;
};
```

```Output
money_put( ) = "CAD1,000.12"
```

## <a name="string_type"></a>  money_put::string_type

一种类型，此类型描述包含 `CharType` 类型字符的字符串。

```cpp
typedef basic_string<CharType, Traits, Allocator> string_type;
```

### <a name="remarks"></a>备注

此类型描述 [basic_string](../standard-library/basic-string-class.md) 模板类的专用化，该模板类的对象可存储来自源序列的元素序列。

## <a name="see-also"></a>请参阅

[\<locale>](../standard-library/locale.md)<br/>
[facet 类](../standard-library/locale-class.md#facet_class)<br/>
[C++ 标准库中的线程安全](../standard-library/thread-safety-in-the-cpp-standard-library.md)<br/>
