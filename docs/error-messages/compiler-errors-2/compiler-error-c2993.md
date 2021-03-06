---
title: 编译器错误 C2993 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2993
dev_langs:
- C++
helpviewer_keywords:
- C2993
ms.assetid: 4ffd2b78-654b-46aa-95a6-b62101cf91c8
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 09b3c789cc15d2e146f1c5031003fc74d783e827
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2018
ms.locfileid: "46081932"
---
# <a name="compiler-error-c2993"></a>编译器错误 C2993

identifier： 非类型模板参数 parameter 的非法类型

不能声明具有结构或联合的自变量的模板。 使用指针将作为模板参数中传递的结构和联合。

下面的示例生成 C2993:

```
// C2993.cpp
// compile with: /c
// C2993 expected
struct MyStruct {
   int a;char b;
};

template <class T, struct MyStruct S>   // C2993

// try the following line instead
// template <class T, struct MyStruct * S>
class CMyClass {};
```

此错误还将生成的 Visual Studio.NET 2003年执行的编译器一致性工作： 浮点，不再允许使用非类型模板参数。 C + + 标准不允许浮点非类型模板参数。

如果它是一个函数模板，使用函数自变量传入浮动点 （此代码将在 Visual c + + 的 Visual Studio.NET 2003年和 Visual Studio.NET 版本中有效） 的非类型模板参数。 如果它是类模板，没有简单的解决方法。

```
// C2993b.cpp
// compile with: /c
template<class T, float f> void func(T) {}   // C2993

// OK
template<class T>   void func2(T, float) {}
```