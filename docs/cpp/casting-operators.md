---
title: 强制转换运算符 |Microsoft Docs
ms.custom: index-page
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- operators [C++], casting
- casting operators [C++]
ms.assetid: 16240348-26bc-4f77-8eab-57253f00ce52
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 341812299d8cf95e351a087e9957dc0425cb25b2
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2018
ms.locfileid: "46075938"
---
# <a name="casting-operators"></a>强制转换运算符

有几种特定于 C++ 语言的转换运算符。 这些运算符用于删除旧式 C 语言转换中的一些多义性和危险继承。 这些运算符是：

- [dynamic_cast](../cpp/dynamic-cast-operator.md)用于多态类型的转换。

- [static_cast](../cpp/static-cast-operator.md)用于非多态类型的转换。

- [const_cast](../cpp/const-cast-operator.md)用于删除**const**，**易失性**，并且 **__unaligned**属性。

- [reinterpret_cast](../cpp/reinterpret-cast-operator.md)用于位的简单重新解释。

- [safe_cast](../windows/safe-cast-cpp-component-extensions.md)用于生成可验证的 MSIL。

使用**const_cast**并**reinterpret_cast**作为最后的手段，因为这些运算符带来的危险相同为旧的样式转换。 但是，若要完全替换旧的样式转换，仍必须使用它们。

## <a name="see-also"></a>请参阅

[强制转换](../cpp/casting.md)