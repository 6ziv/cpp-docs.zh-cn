---
title: '&lt;ostream&gt; 函数 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- ostream/std::swap
- ostream/std::endl
- ostream/std::ends
- ostream/std::flush
ms.assetid: d6e56cc0-c8df-4dbe-be10-98e14c35ed3a
helpviewer_keywords:
- std::swap [C++]
- std::endl [C++]
- std::ends [C++]
- std::flush [C++]
ms.openlocfilehash: 494c750ec80000ef9090824e0436f6e443593847
ms.sourcegitcommit: 761c5f7c506915f5a62ef3847714f43e9b815352
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2018
ms.locfileid: "44107598"
---
# <a name="ltostreamgt-functions"></a>&lt;ostream&gt; 函数

这些是中定义的全局模板函数&lt;ostream&gt;。 成员函数，请参阅[basic_ostream 类](basic-ostream-class.md)文档。

||||
|-|-|-|
|[endl](#endl)|[ends](#ends)|[flush](#flush)|
|[swap](#swap)|

## <a name="endl"></a>endl

终止行并刷新缓冲区。

```cpp
template class<Elem, Tr>
basic_ostream<Elem, Tr>& endl(
   basic_ostream<Elem, Tr>& Ostr);
```

### <a name="parameters"></a>参数

*Elem*<br/>
元素类型。

*Ostr*<br/>
类型的对象**basic_ostream**。

*Tr*<br/>
字符特征。

### <a name="return-value"></a>返回值

类型的对象**basic_ostream**。

### <a name="remarks"></a>备注

该操控器调用*Ostr*。[将放](../standard-library/basic-ostream-class.md#put)(*Ostr*。[扩大](../standard-library/basic-ios-class.md#widen)('\n'))，然后调用*Ostr*。[刷新](../standard-library/basic-ostream-class.md#flush)。 它将返回*Ostr*。

### <a name="example"></a>示例

```cpp
// ostream_endl.cpp
// compile with: /EHsc
#include <iostream>

int main( )
{
   using namespace std;
   cout << "testing" << endl;
}
```

```Output
testing
```

## <a name="ends"></a>结尾

终止字符串。

```cpp
template class<Elem, Tr>
basic_ostream<Elem, Tr>& ends(
   basic_ostream<Elem, Tr>& Ostr);
```

### <a name="parameters"></a>参数

*Elem*<br/>
元素类型。

*Ostr*<br/>
一个 `basic_ostream` 类型的对象。

*Tr*<br/>
字符特征。

### <a name="return-value"></a>返回值

一个 `basic_ostream` 类型的对象。

### <a name="remarks"></a>备注

该操控器调用*Ostr*。[将放](../standard-library/basic-ostream-class.md#put)(*Elem*(\0))。 它将返回*Ostr*。

### <a name="example"></a>示例

```cpp
// ostream_ends.cpp
// compile with: /EHsc
#include <iostream>

int main( )
{
   using namespace std;
   cout << "a";
   cout << "b" << ends;
   cout << "c" << endl;
}
```

```Output
ab c
```

## <a name="flush"></a>flush

刷新缓冲区。

```cpp
template class<Elem, Tr>
basic_ostream<Elem, Tr>& flush(
   basic_ostream<Elem, Tr>& Ostr);
```

### <a name="parameters"></a>参数

*Elem*<br/>
元素类型。

*Ostr*<br/>
一个 `basic_ostream` 类型的对象。

*Tr*<br/>
字符特征。

### <a name="return-value"></a>返回值

一个 `basic_ostream` 类型的对象。

### <a name="remarks"></a>备注

该操控器调用*Ostr*。[刷新](../standard-library/basic-ostream-class.md#flush)。 它将返回*Ostr*。

### <a name="example"></a>示例

```cpp
// ostream_flush.cpp
// compile with: /EHsc
#include <iostream>

int main( )
{
   using namespace std;
   cout << "testing" << flush;
}
```

```Output
testing
```

## <a name="swap"></a>swap

交换两个 `basic_ostream` 对象的值。

```cpp
template <class Elem, class Tr>
void swap(
   basic_ostream<Elem, Tr>& left,
   basic_ostream<Elem, Tr>& right);
```

### <a name="parameters"></a>参数

*Elem*<br/>
元素类型。

*Tr*<br/>
字符特征。

*left*<br/>
对 `basic_ostream` 对象的左值引用。

*right*<br/>
对 `basic_ostream` 对象的左值引用。

### <a name="remarks"></a>备注

模板函数 `swap` 执行 `left.swap(right)`。

## <a name="see-also"></a>请参阅

[\<ostream>](../standard-library/ostream.md)
