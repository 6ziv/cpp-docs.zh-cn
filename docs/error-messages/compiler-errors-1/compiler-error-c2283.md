---
title: 编译器错误 C2283 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2283
dev_langs:
- C++
helpviewer_keywords:
- C2283
ms.assetid: 8a5b3175-b480-4598-a1f7-0b50504c5caa
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 9c90c355a1c2ecd19ccd7b2fc25e75f53d4f9414
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2018
ms.locfileid: "46070114"
---
# <a name="compiler-error-c2283"></a>编译器错误 C2283

“identifier”：未命名的结构上不允许使用纯说明符或抽象重写说明符

使用纯说明符声明了未命名类或结构的成员函数，这是不允许的。

以下示例生成 C2283：

```
// C2283.cpp
// compile with: /c
struct {
   virtual void func() = 0;   // C2283
};
struct T {
   virtual void func() = 0;   // OK
};
```