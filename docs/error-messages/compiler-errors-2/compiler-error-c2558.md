---
title: 编译器错误 C2558 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2558
dev_langs:
- C++
helpviewer_keywords:
- C2558
ms.assetid: 822b701e-dcae-423a-b21f-47f36aff9c90
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: fd6f38ff8fbe0c4179addf46a43a35be4237b73e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2018
ms.locfileid: "46100833"
---
# <a name="compiler-error-c2558"></a>编译器错误 C2558

“identifier”: 没有可用的复制构造函数或复制构造函数声明为“explicit”

复制构造函数从同一类型的另一个对象初始化某对象。 （它生成源对象的副本。）如果没有定义任何构造函数，则编译器生成默认复制构造函数。

### <a name="to-fix-this-error"></a>修复此错误的方法

1. 在尝试复制其复制构造函数为 `private` 的类时，可能出现该问题。 在大多数情况下，不应复制具有 `private` 复制构造函数的类。 通用编程技术声明 `private` 复制构造函数以防止直接使用类。 该类本身可能无用，或需要另一个类才能正常工作。

     如果确定可安全地使用具有 `private` 复制构造函数的类，请从该具有 `private` 构造函数的类派生一个新类，并使 `public` 或 `protected` 复制构造函数在该新类中可用。 使用该派生类替代原始类。

1. 在尝试复制其复制构造函数为显式的类时，可能出现该问题。 将复制构造函数声明为 `explicit` 会阻止将类的对象传递到对象或从函数到类的对象。 有关显式构造函数的详细信息，请参阅[用户定义类型的转换](../../cpp/user-defined-type-conversions-cpp.md)。

1. 当尝试复制使用不采用 `const` 引用参数声明 `const` 的类实例时，可能出现该问题。 请使用 `const` 类型引用而不是非常量类型引用声明复制构造函数。