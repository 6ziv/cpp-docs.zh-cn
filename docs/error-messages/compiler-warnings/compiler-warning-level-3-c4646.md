---
title: 编译器警告 （等级 3） C4646 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4646
dev_langs:
- C++
helpviewer_keywords:
- C4646
ms.assetid: 23677e8e-603e-40e0-b99a-2e4894a1278e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 9ad9a96aaf15294a1404de54f276eb5309a09357
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2018
ms.locfileid: "46086769"
---
# <a name="compiler-warning-level-3-c4646"></a>编译器警告（等级 3）C4646

用 __declspec(noreturn) 声明的函数有非 void 返回类型

标记有 [noreturn](../../cpp/noreturn.md) `__declspec` 修饰符的函数应有 [void](../../cpp/void-cpp.md) 返回类型。

下面的示例生成 C4646：

```
// C4646.cpp
// compile with: /W3 /WX
int __declspec(noreturn) TestFunction()
{   // C4646  make return type void
}
```