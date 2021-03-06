---
title: no_injected_text |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- vc-attr.no_injected_text
dev_langs:
- C++
helpviewer_keywords:
- no_injected_text attribute
ms.assetid: 5256f808-e41e-4f4a-9ea5-e447919f5696
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 2cd7288b4475197d9980aab2eb9037419304c0fd
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/19/2018
ms.locfileid: "46442924"
---
# <a name="noinjectedtext"></a>no_injected_text

禁止编译器注入代码作为特性使用结果。

## <a name="syntax"></a>语法

```cpp
[ no_injected_text(
   boolean
) ];
```

### <a name="parameters"></a>参数

*一个布尔值*<br/>
（可选）**，则返回 true**如果你想注入，没有代码**false**若要允许代码注入。 **true**是默认值。

## <a name="remarks"></a>备注

最常见用法**no_injected_text** c + + 属性是通过[/Fx](../build/reference/fx-merge-injected-code.md)编译器选项，将插入**no_injected_text**属性拖动到.mrg 文件。

## <a name="requirements"></a>要求

### <a name="attribute-context"></a>特性上下文

|||
|-|-|
|**适用对象**|任何位置|
|**可重复**|否|
|**必需的特性**|无|
|**无效的特性**|无|

有关特性上下文的详细信息，请参见 [特性上下文](../windows/attribute-contexts.md)。

## <a name="see-also"></a>请参阅

[编译器特性](../windows/compiler-attributes.md)  