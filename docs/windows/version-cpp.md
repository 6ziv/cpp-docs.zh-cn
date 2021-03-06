---
title: 版本 （c + +） |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- vc-attr.version
dev_langs:
- C++
helpviewer_keywords:
- version attribute
- version information, version attribute
ms.assetid: db6ce5d8-82c2-4329-b1a8-8ca2f67342cb
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 60a5ad42f83d9e9528fd5bdc4c8d3e62254a3677
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/19/2018
ms.locfileid: "46438727"
---
# <a name="version-c"></a>version (C++)

标识类的多个版本间的特定版本。

## <a name="syntax"></a>语法

```cpp
[ version(
   "version"
) ]
```

### <a name="parameters"></a>参数

*version*<br/>
版本号`coclass`。 如果未指定，则将在.idl 文件中放置 1.0。

## <a name="remarks"></a>备注

**版本**c + + 属性具有相同的功能[版本](/windows/desktop/Midl/version)MIDL 特性并将传递给生成的.idl 文件。

## <a name="example"></a>示例

请参阅[可绑定](../windows/bindable.md)的示例使用的示例**版本**。

## <a name="requirements"></a>要求

### <a name="attribute-context"></a>特性上下文

|||
|-|-|
|**适用对象**|**类**，**结构**|
|**可重复**|否|
|**必需的特性**|**coclass**|
|**无效的特性**|无|

有关特性上下文的详细信息，请参见 [特性上下文](../windows/attribute-contexts.md)。

## <a name="see-also"></a>请参阅

[编译器特性](../windows/compiler-attributes.md)<br/>
[类特性](../windows/class-attributes.md)  