---
title: 编译器错误 C3196 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3196
dev_langs:
- C++
helpviewer_keywords:
- C3196
ms.assetid: d9c38a13-191d-472d-aa2b-f61a6459d16c
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 256c76bf66906ef43afdc3574b819bd7cf5df1cb
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2018
ms.locfileid: "46045896"
---
# <a name="compiler-error-c3196"></a>编译器错误 C3196

keyword： 使用了多次

不止一次使用的关键字。

下面的示例生成 C3196:

```
// C3196.cpp
// compile with: /clr
ref struct R abstract abstract {};   // C3196
ref struct S abstract {};   // OK
```