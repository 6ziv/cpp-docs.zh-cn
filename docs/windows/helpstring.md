---
title: helpstring |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- vc-attr.helpstring
dev_langs:
- C++
helpviewer_keywords:
- helpstring attribute [C++]
ms.assetid: 0401e905-a63e-4fad-98d0-d1efea111966
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 2892f957cf8937b5b030e7624bf3e39f546a7103
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/19/2018
ms.locfileid: "46437596"
---
# <a name="helpstring"></a>helpstring

指定一个字符串，用于描述应用该字符串的元素。

## <a name="syntax"></a>语法

```cpp
[ helpstring(
   "string"
) ]
```

### <a name="parameters"></a>参数

*string*<br/>
帮助字符串的文本。

## <a name="remarks"></a>备注

**Helpstring** c + + 属性具有相同的功能[helpstring](/windows/desktop/Midl/helpstring) MIDL 特性。

## <a name="example"></a>示例

有关示例，请参阅[defaultvalue](../windows/defaultvalue.md)有关如何使用的示例**helpstring**。

## <a name="requirements"></a>要求

### <a name="attribute-context"></a>特性上下文

|||
|-|-|
|**适用对象**|**接口**， **typedef**，**类**，方法、 属性|
|**可重复**|否|
|**必需的特性**|无|
|**无效的特性**|无|

有关详细信息，请参见 [特性上下文](../windows/attribute-contexts.md)。

## <a name="see-also"></a>请参阅

[IDL 特性](../windows/idl-attributes.md)<br/>
[接口特性](../windows/interface-attributes.md)<br/>
[类特性](../windows/class-attributes.md)<br/>
[方法特性](../windows/method-attributes.md)<br/>
[Typedef、Enum、Union 和 Struct 特性](../windows/typedef-enum-union-and-struct-attributes.md)<br/>
[helpfile](../windows/helpfile.md)<br/>
[helpcontext](../windows/helpcontext.md)  