---
title: 实用工具 (STL/CLR) |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: reference
f1_keywords:
- <cliext/utility>
- cliext::pair
- cliext::pair::pair
- cliext::pair::first
- cliext::pair::first_type
- cliext::pair::second
- cliext::pair::second_type
- cliext::pair::swap
- cliext::make_pair
- cliext::pair::operator=
- cliext::pair::operator==
- cliext::pair::operator>=
- cliext::pair::operator>
- cliext::pair::operator!=
- cliext::pair::operator<=
- cliext::pair::operator<
dev_langs:
- C++
helpviewer_keywords:
- <utility> header [STL/CLR]
- utility header [STL/CLR]
- <cliext/utility> header [STL/CLR]
- first member [STL/CLR]
- first_type member [STL/CLR]
- second member [STL/CLR]
- second_type member [STL/CLR]
- swap member [STL/CLR]
- make_pair function [STL/CLR]
- pair class [STL/CLR]
- pair member [STL/CLR]
- operator== member [STL/CLR]
- operator= member [STL/CLR]
- operator>= member [STL/CLR]
- operator> member [STL/CLR]
- operator!= member [STL/CLR]
- operator<= member [STL/CLR]
- operator< member [STL/CLR]
ms.assetid: fb48cb75-d5ef-47ce-b526-bf60dc86c552
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 931e0561a57cd65b8f0f9204eb08e4df99c0150e
ms.sourcegitcommit: e9ce38decc9f986edab5543de3464b11ebccb123
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/13/2018
ms.locfileid: "42573202"
---
# <a name="utility-stlclr"></a>utility (STL/CLR)
包含 STL/CLR 标头`<cliext/utility>`来定义模板类`pair`和多个支持模板函数。  
  
## <a name="syntax"></a>语法  
  
```cpp  
#include <utility>  
```

## <a name="requirements"></a>要求  
 **标头：** \<cliext/实用程序 >  
  
 **Namespace:** cliext  
  
## <a name="declarations"></a>声明  
  
|类|描述|  
|-----------|-----------------|  
|[pair (STL/CLR)](#pair)|换行一的对元素。|  
  
|运算符|描述|  
|--------------|-----------------|  
|[operator== (pair) (STL/CLR)](#op_eq)|对相等比较。|  
|[operator!= (pair) (STL/CLR)](#op_neq)|对不相等比较。|  
|[operator< (pair) (STL/CLR)](#op_lt)|对小于比较。|  
|[运算符\<= （对） (STL/CLR)](#op_lteq)|配对小于或等于比较。|  
|[operator> (pair) (STL/CLR)](#op_gt)|对大于比较。|  
|[operator>= (pair) (STL/CLR)](#op_gteq)|对大于或等于比较。|  
  
|函数|描述|  
|--------------|-----------------|  
|[make_pair (STL/CLR)](#make_pair)|请从一对值对。|  

## <a name="members"></a>成员

##<a name="pair"></a> 对 (STL/CLR)
此模板类描述包装一对值的对象。  
  
### <a name="syntax"></a>语法  
  
```cpp  
template<typename Value1,  
    typename Value2>  
    ref class pair;  
```  
  
#### <a name="parameters"></a>参数  
 *值 1*  
 第一个已包装的值的类型。  
  
 *Value2*  
 第二个包装值的类型。  
  
## <a name="members"></a>成员  
  
|类型定义|描述|  
|---------------------|-----------------|  
|[pair::first_type (STL/CLR)](#first_type)|第一个已包装的值的类型。|  
|[pair::second_type (STL/CLR)](#second_type)|第二个包装值的类型。|  
  
|成员对象|描述|  
|-------------------|-----------------|  
|[pair::first (STL/CLR)](#first)|第一个存储的值。|  
|[pair::second (STL/CLR)](#second)|第二个存储的值。|  
  
|成员函数|描述|  
|---------------------|-----------------|  
|[pair::pair (STL/CLR)](#pair_pair)|构造对对象。|  
|[pair::swap (STL/CLR)](#swap)|交换两个对中的内容。|  
  
|运算符|描述|  
|--------------|-----------------|  
|[pair::operator= (STL/CLR)](#op_as)|替换存储的值对。|  
  
## <a name="remarks"></a>备注  
 该对象存储值的对。 使用此模板类，将两个值合并到单个对象。 此外，该对象`cliext::pair`（此处所述） 存储仅托管类型; 若要保存对非托管的类型，请使用`std::pair`中声明`<utility>`。  


## <a name="first"></a> pair::first (STL/CLR)
第一个包装的值。  
  
### <a name="syntax"></a>语法  
  
```cpp  
Value1 first;  
```  
  
### <a name="remarks"></a>备注  
 该对象存储第一个已包装的值。  
  
### <a name="example"></a>示例  
  
```cpp  
// cliext_pair_first.cpp   
// compile with: /clr   
#include <cliext/utility>   
  
int main()   
    {   
    cliext::pair<wchar_t, int> c1(L'x', 3);   
    System::Console::WriteLine("[{0}, {1}]", c1.first, c1.second);   
  
    cliext::pair<wchar_t, int>::first_type first_val = c1.first;   
    cliext::pair<wchar_t, int>::second_type second_val = c1.second;   
    System::Console::WriteLine("[{0}, {1}]", first_val, second_val);   
    return (0);   
    }  
```  
  
```Output  
[x, 3]  
```  

## <a name="first_type"></a> pair::first_type (STL/CLR)
第一个已包装的值的类型。  
  
### <a name="syntax"></a>语法  
  
```cpp  
typedef Value1 first_type;  
```  
  
### <a name="remarks"></a>备注  
 该类型是模板参数的同义词*Value1*。  
  
### <a name="example"></a>示例  
  
```cpp  
// cliext_pair_first_type.cpp   
// compile with: /clr   
#include <cliext/utility>   
  
int main()   
    {   
    cliext::pair<wchar_t, int> c1(L'x', 3);   
    System::Console::WriteLine("[{0}, {1}]", c1.first, c1.second);   
  
    cliext::pair<wchar_t, int>::first_type first_val = c1.first;   
    cliext::pair<wchar_t, int>::second_type second_val = c1.second;   
    System::Console::WriteLine("[{0}, {1}]", first_val, second_val);   
    return (0);   
    }   
```  
  
```Output  
[x, 3]  
```  

## <a name="op_as"></a> pair::operator = (STL/CLR)
替换存储的值对。  
  
### <a name="syntax"></a>语法  
  
```cpp  
pair<Value1, Value2>% operator=(pair<Value1, Value2>% right);  
```  
  
#### <a name="parameters"></a>参数  
 *right*  
 若要复制的对。  
  
### <a name="remarks"></a>备注  
 成员运算符副本*右*对象，然后返回`*this`。 用于存储对中的值的副本替换存储的值对*右*。  
  
### <a name="example"></a>示例  
  
```cpp  
// cliext_pair_operator_as.cpp   
// compile with: /clr   
#include <cliext/utility>   
  
int main()   
    {   
    cliext::pair<wchar_t, int> c1(L'x', 3);   
    System::Console::WriteLine("[{0}, {1}]", c1.first, c1.second);   
  
// assign to a new pair   
    cliext::pair<wchar_t, int> c2;   
    c2 = c1;   
    System::Console::WriteLine("[{0}, {1}]", c2.first, c2.second);   
    return (0);   
    }   
```  
  
```Output  
[x, 3]  
[x, 3]  
```  

## <a name="pair_pair"></a> pair::pair (STL/CLR)
构造对对象。  
  
### <a name="syntax"></a>语法  
  
```cpp  
pair();  
pair(pair<Coll>% right);  
pair(pair<Coll>^ right);  
pair(Value1 val1, Value2 val2);  
```  
  
#### <a name="parameters"></a>参数  
 *right*  
 要存储对。  
  
 *Val1*  
 要存储的第一个值。  
  
 *Val2*  
 要存储的第二个值。  
  
### <a name="remarks"></a>备注  
 构造函数：  
  
 `pair();`  
  
 初始化使用默认构造值的存储的对。  
  
 构造函数：  
  
 `pair(pair<Value1, Value2>% right);`  
  
 初始化具有存储的对`right.` [pair::first (STL/CLR)](../dotnet/pair-first-stl-clr.md)并`right.` [pair::second (STL/CLR)](../dotnet/pair-second-stl-clr.md)。  
  
 `pair(pair<Value1, Value2>^ right);`  
  
 初始化具有存储的对`right->` [pair::first (STL/CLR)](../dotnet/pair-first-stl-clr.md)并`right>` [pair::second (STL/CLR)](../dotnet/pair-second-stl-clr.md)。  
  
 构造函数：  
  
 `pair(Value1 val1, Value2 val2);`  
  
 初始化具有存储的对*val1*并*val2*。  
  
### <a name="example"></a>示例  
  
```cpp  
// cliext_pair_construct.cpp   
// compile with: /clr   
#include <cliext/utility>   
  
int main()   
    {   
// construct an empty container   
    cliext::pair<wchar_t, int> c1;   
    System::Console::WriteLine("[{0}, {1}]",   
        c1.first == L'\0' ? "\\0" : "??", c1.second);   
  
// construct with a pair of values   
    cliext::pair<wchar_t, int> c2(L'x', 3);   
    System::Console::WriteLine("[{0}, {1}]", c2.first, c2.second);   
  
// construct by copying another pair   
    cliext::pair<wchar_t, int> c3(c2);   
    System::Console::WriteLine("[{0}, {1}]", c3.first, c3.second);   
  
// construct by copying a pair handle   
    cliext::pair<wchar_t, int> c4(%c3);   
    System::Console::WriteLine("[{0}, {1}]", c4.first, c4.second);   
  
    return (0);   
    }   
```  
  
```Output  
[\0, 0]  
[x, 3]  
[x, 3]  
[x, 3]  
```  

## <a name="second"></a> pair::second (STL/CLR)
第二个包装值。  
  
### <a name="syntax"></a>语法  
  
```cpp  
Value2 second;  
```  
  
### <a name="remarks"></a>备注  
 该对象存储第二个包装的值。  
  
### <a name="example"></a>示例  
  
```cpp  
// cliext_pair_second.cpp   
// compile with: /clr   
#include <cliext/utility>   
  
int main()   
    {   
    cliext::pair<wchar_t, int> c1(L'x', 3);   
    System::Console::WriteLine("[{0}, {1}]", c1.first, c1.second);   
  
    cliext::pair<wchar_t, int>::first_type first_val = c1.first;   
    cliext::pair<wchar_t, int>::second_type second_val = c1.second;   
    System::Console::WriteLine("[{0}, {1}]", first_val, second_val);   
    return (0);   
    }  
```  
  
```Output  
[x, 3]  
```  

## <a name="second_type"></a> pair::second_type (STL/CLR)
第二个包装值的类型。  
  
### <a name="syntax"></a>语法  
  
```cpp  
typedef Value2 second_type;  
```  
  
### <a name="remarks"></a>备注  
 该类型是模板参数的同义词*Value2*。  
  
### <a name="example"></a>示例  
  
```cpp  
// cliext_pair_second_type.cpp   
// compile with: /clr   
#include <cliext/utility>   
  
int main()   
    {   
    cliext::pair<wchar_t, int> c1(L'x', 3);   
    System::Console::WriteLine("[{0}, {1}]", c1.first, c1.second);   
  
    cliext::pair<wchar_t, int>::first_type first_val = c1.first;   
    cliext::pair<wchar_t, int>::second_type second_val = c1.second;   
    System::Console::WriteLine("[{0}, {1}]", first_val, second_val);   
    return (0);   
    }   
```  
  
```Output  
[x, 3]  
```    

## <a name="swap"></a> pair::swap (STL/CLR)
交换两个对中的内容。  
  
### <a name="syntax"></a>语法  
  
```cpp  
void swap(pair<Value1, Value2>% right);  
```  
  
#### <a name="parameters"></a>参数  
 *right*  
 对要与其交换内容。  
  
### <a name="remarks"></a>备注  
 成员函数交换存储的之间的值对`*this`并*右*。  
  
### <a name="example"></a>示例  
  
```cpp  
// cliext_pair_swap.cpp   
// compile with: /clr   
#include <cliext/adapter>   
#include <cliext/deque>   
  
typedef cliext::collection_adapter<   
    System::Collections::ICollection> Mycoll;   
int main()   
    {   
    cliext::deque<wchar_t> d1;   
    d1.push_back(L'a');   
    d1.push_back(L'b');   
    d1.push_back(L'c');   
    Mycoll c1(%d1);   
  
// display initial contents " a b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// construct another container with repetition of values   
    cliext::deque<wchar_t> d2(5, L'x');   
    Mycoll c2(%d2);   
    for each (wchar_t elem in c2)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// swap and redisplay   
    c1.swap(c2);   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
    for each (wchar_t elem in c2)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }   
```  
  
```Output  
a b c  
x x x x x  
x x x x x  
a b c  
```  

## <a name="make_pair"></a> make_pair (STL/CLR)
使`pair`从一对的值。  
  
### <a name="syntax"></a>语法  
  
```cpp  
template<typename Value1,  
    typename Value2>  
    pair<Value1, Value2> make_pair(Value1 first, Value2 second);  
```  
  
#### <a name="parameters"></a>参数  
 *值 1*  
 第一个已包装的值的类型。  
  
 *Value2*  
 第二个包装值的类型。  
  
 *first*  
 要包装的第一个值。  
  
 *second*  
 要包装的第二个值。  
  
### <a name="remarks"></a>备注  
 此模板函数返回 `pair<Value1, Value2>(first, second)`。 用于构造`pair<Value1, Value2>`从一对值的对象。  
  
### <a name="example"></a>示例  
  
```cpp  
// cliext_make_pair.cpp   
// compile with: /clr   
#include <cliext/utility>   
  
int main()   
    {   
    cliext::pair<wchar_t, int> c1(L'x', 3);   
    System::Console::WriteLine("[{0}, {1}]", c1.first, c1.second);   
  
    c1 = cliext::make_pair(L'y', 4);   
    System::Console::WriteLine("[{0}, {1}]", c1.first, c1.second);   
    return (0);   
    }  
```  
  
```Output  
[x, 3]  
[y, 4]  
```  

## <a name="op_neq"></a> 运算符 ！ = （对） (STL/CLR)
对不相等比较。  
  
### <a name="syntax"></a>语法  
  
```cpp  
template<typename Value1,  
    typename Value2>  
    bool operator!=(pair<Value1, Value2>% left,  
        pair<Value1, Value2>% right);  
```  
  
#### <a name="parameters"></a>参数  
 *left*  
 要比较的左的对。  
  
 *right*  
 要比较的右对。  
  
### <a name="remarks"></a>备注  
 运算符函数返回`!(left == right)`。 使用它来测试是否*左*未排序相同*右*当两个对都比较的元素的方式。  
  
### <a name="example"></a>示例  
  
```cpp
// cliext_pair_operator_ne.cpp   
// compile with: /clr   
#include <cliext/utility>   
  
int main()   
    {   
    cliext::pair<wchar_t, int> c1(L'x', 3);   
    System::Console::WriteLine("[{0}, {1}]", c1.first, c1.second);   
    cliext::pair<wchar_t, int> c2(L'x', 4);   
    System::Console::WriteLine("[{0}, {1}]", c2.first, c2.second);   
  
    System::Console::WriteLine("[x 3] != [x 3] is {0}",   
        c1 != c1);   
    System::Console::WriteLine("[x 3] != [x 4] is {0}",   
        c1 != c2);   
    return (0);   
    }   
```  
  
```Output  
[x, 3]  
[x, 4]  
[x 3] != [x 3] is False  
[x 3] != [x 4] is True  
```  
  
## <a name="op_lt"></a> 运算符&lt;（对） (STL/CLR)
对小于比较。  
  
### <a name="syntax"></a>语法  
  
```cpp  
template<typename Value1,  
    typename Value2>  
    bool operator<(pair<Value1, Value2>% left,  
        pair<Value1, Value2>% right);  
```  
  
#### <a name="parameters"></a>参数  
 *left*  
 要比较的左的对。  
  
 *right*  
 要比较的右对。  
  
### <a name="remarks"></a>备注  
 运算符函数将返回`left.first <` `right.first || !(right.first <` `left.first &&` `left.second <` `right.second`。 使用它来测试是否*左*进行排序之前*右*当两个对都比较的元素的方式。  
  
### <a name="example"></a>示例  
  
```cpp  
// cliext_pair_operator_lt.cpp   
// compile with: /clr   
#include <cliext/utility>   
  
int main()   
    {   
    cliext::pair<wchar_t, int> c1(L'x', 3);   
    System::Console::WriteLine("[{0}, {1}]", c1.first, c1.second);   
    cliext::pair<wchar_t, int> c2(L'x', 4);   
    System::Console::WriteLine("[{0}, {1}]", c2.first, c2.second);   
  
    System::Console::WriteLine("[x 3] < [x 3] is {0}",   
        c1 < c1);   
    System::Console::WriteLine("[x 3] < [x 4] is {0}",   
        c1 < c2);   
    return (0);   
    }   
```  
  
```Output  
[x, 3]  
[x, 4]  
[x 3] < [x 3] is False  
[x 3] < [x 4] is True  
```  

## <a name="op_lteq"></a> 运算符&lt;= （对） (STL/CLR)
配对小于或等于比较。  
  
### <a name="syntax"></a>语法  
  
```cpp  
template<typename Value1,  
    typename Value2>  
    bool operator<=(pair<Value1, Value2>% left,  
        pair<Value1, Value2>% right);  
```  
  
#### <a name="parameters"></a>参数  
 *left*  
 要比较的左的对。  
  
 *right*  
 要比较的右对。  
  
### <a name="remarks"></a>备注  
 运算符函数返回`!(right < left)`。 使用它来测试是否*左*未排序后*右*当两个对都比较的元素的方式。  
  
### <a name="example"></a>示例  
  
```cpp  
// cliext_pair_operator_le.cpp   
// compile with: /clr   
#include <cliext/utility>   
  
int main()   
    {   
    cliext::pair<wchar_t, int> c1(L'x', 3);   
    System::Console::WriteLine("[{0}, {1}]", c1.first, c1.second);   
    cliext::pair<wchar_t, int> c2(L'x', 4);   
    System::Console::WriteLine("[{0}, {1}]", c2.first, c2.second);   
  
    System::Console::WriteLine("[x 3] <= [x 3] is {0}",   
        c1 <= c1);   
    System::Console::WriteLine("[x 4] <= [x 3] is {0}",   
        c2 <= c1);   
    return (0);   
    }   
```  
  
```Output  
[x, 3]  
[x, 4]  
[x 3] <= [x 3] is True  
[x 4] <= [x 3] is False  
```  
  
## <a name="op_eq"></a> 运算符 = = （对） (STL/CLR)
对相等比较。  
  
### <a name="syntax"></a>语法  
  
```cpp  
template<typename Value1,  
    typename Value2>  
    bool operator==(pair<Value1, Value2>% left,  
        pair<Value1, Value2>% right);  
```  
  
#### <a name="parameters"></a>参数  
 *left*  
 要比较的左的对。  
  
 *right*  
 要比较的右对。  
  
### <a name="remarks"></a>备注  
 运算符函数将返回`left.first ==` `right.first &&` `left.second ==` `right.second`。 使用它来测试是否*左*进行排序相同*右*当两个对都比较的元素的方式。  
  
### <a name="example"></a>示例  
  
```cpp  
// cliext_pair_operator_eq.cpp   
// compile with: /clr   
#include <cliext/utility>   
  
int main()   
    {   
    cliext::pair<wchar_t, int> c1(L'x', 3);   
    System::Console::WriteLine("[{0}, {1}]", c1.first, c1.second);   
    cliext::pair<wchar_t, int> c2(L'x', 4);   
    System::Console::WriteLine("[{0}, {1}]", c2.first, c2.second);   
  
    System::Console::WriteLine("[x 3] == [x 3] is {0}",   
        c1 == c1);   
    System::Console::WriteLine("[x 3] == [x 4] is {0}",   
        c1 == c2);   
    return (0);   
    }   
```  
  
```Output  
[x, 3]  
[x, 4]  
[x 3] == [x 3] is True  
[x 3] == [x 4] is False  
```  

## <a name="op_gt"></a> 运算符&gt;（对） (STL/CLR)
对大于比较。  
  
### <a name="syntax"></a>语法  
  
```cpp  
template<typename Value1,  
    typename Value2>  
    bool operator>(pair<Value1, Value2>% left,  
        pair<Value1, Value2>% right);  
```  
  
#### <a name="parameters"></a>参数  
 *left*  
 要比较的左的对。  
  
 *right*  
 要比较的右对。  
  
### <a name="remarks"></a>备注  
 运算符函数将返回`right` `<` `left`。 使用它来测试是否*左*进行排序后*右*当两个对都比较的元素的方式。  
  
### <a name="example"></a>示例  
  
```cpp  
// cliext_pair_operator_gt.cpp   
// compile with: /clr   
#include <cliext/utility>   
  
int main()   
    {   
    cliext::pair<wchar_t, int> c1(L'x', 3);   
    System::Console::WriteLine("[{0}, {1}]", c1.first, c1.second);   
    cliext::pair<wchar_t, int> c2(L'x', 4);   
    System::Console::WriteLine("[{0}, {1}]", c2.first, c2.second);   
  
    System::Console::WriteLine("[x 3] > [x 3] is {0}",   
        c1 > c1);   
    System::Console::WriteLine("[x 4] > [x 3] is {0}",   
        c2 > c1);   
    return (0);   
    }   
```  
  
```Output  
[x, 3]  
[x, 4]  
[x 3] > [x 3] is False  
[x 4] > [x 3] is True  
```  

## <a name="op_gteq"></a> 运算符&gt;= （对） (STL/CLR)
对大于或等于比较。  
  
### <a name="syntax"></a>语法  
  
```cpp  
template<typename Value1,  
    typename Value2>  
    bool operator>=(pair<Value1, Value2>% left,  
        pair<Value1, Value2>% right);  
```  
  
#### <a name="parameters"></a>参数  
 *left*  
 要比较的左的对。  
  
 *right*  
 要比较的右对。  
  
### <a name="remarks"></a>备注  
 运算符函数返回`!(left < right)`。 使用它来测试是否*左*未排序之前*右*当两个对都比较的元素的方式。  
  
### <a name="example"></a>示例  
  
```cpp  
// cliext_pair_operator_ge.cpp   
// compile with: /clr   
#include <cliext/utility>   
  
int main()   
    {   
    cliext::pair<wchar_t, int> c1(L'x', 3);   
    System::Console::WriteLine("[{0}, {1}]", c1.first, c1.second);   
    cliext::pair<wchar_t, int> c2(L'x', 4);   
    System::Console::WriteLine("[{0}, {1}]", c2.first, c2.second);   
  
    System::Console::WriteLine("[x 3] >= [x 3] is {0}",   
        c1 >= c1);   
    System::Console::WriteLine("[x 3] >= [x 4] is {0}",   
        c1 >= c2);   
    return (0);   
    }   
```  
  
```Output  
[x, 3]  
[x, 4]  
[x 3] >= [x 3] is True  
[x 3] >= [x 4] is False  
``` 