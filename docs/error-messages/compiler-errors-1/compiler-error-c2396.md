---
title: 编译器错误 C2396 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2396
dev_langs:
- C++
helpviewer_keywords:
- C2396
ms.assetid: 1b515ef6-7af4-400f-b4ed-564313ea15f6
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 0d69dfc1e296532f00ce9f44a178a366dca41e2e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2018
ms.locfileid: "46061625"
---
# <a name="compiler-error-c2396"></a>编译器错误 C2396

your_type:: operator'type ': CLR 或 WinRT 用户定义的转换 functionnot 有效。 必须转换自或转换至：“T^”、“T^%”、“T^&”，其中 T =“your_type”

Windows 运行时或托管类型中的转换函数没有至少一个类型与包含转换函数的类型相同的参数。

下面的示例生成 C2396，并演示如何修复此错误：

```
// C2396.cpp
// compile with: /clr /c

ref struct Y {
   static operator int(char c);   // C2396

   // OK
   static operator int(Y^ hY);
   // or
   static operator Y^(char c);
};
```