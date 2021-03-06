---
title: 导入库 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- vc-attr.importlib
dev_langs:
- C++
helpviewer_keywords:
- importlib attribute
ms.assetid: f129e459-b8d3-4aca-a0bc-ee53e18b62ed
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 3df5a1893567b54337a5c3807fcace6a02154670
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/19/2018
ms.locfileid: "46416001"
---
# <a name="importlib"></a>importlib

使已编译到另一个类型库中的类型可供所创建的类型库使用。

## <a name="syntax"></a>语法

```cpp
[ importlib(
   "tlb_file"
) ];
```

### <a name="parameters"></a>参数

*tlb_file*<br/>
要导入当前项目类型库中的 .tlb 文件的名称（用引号引起来）。

## <a name="remarks"></a>备注

**Importlib** c + + 属性会导致`importlib`语句生成的.idl 文件的库块中放置。 **Importlib**属性具有相同的功能[importlib](/windows/desktop/Midl/importlib) MIDL 特性。

## <a name="example"></a>示例

下面的代码演示如何使用的示例**importlib**:

```cpp
// cpp_attr_ref_importlib.cpp
// compile with: /LD
[module(name="MyLib")];
[importlib("importlib.tlb")];
```

## <a name="requirements"></a>要求

### <a name="attribute-context"></a>特性上下文

|||
|-|-|
|**适用对象**|任何位置|
|**可重复**|否|
|**必需的特性**|无|
|**无效的特性**|无|

有关详细信息，请参见 [特性上下文](../windows/attribute-contexts.md)。

## <a name="see-also"></a>请参阅

[编译器特性](../windows/compiler-attributes.md)<br/>
[独立特性](../windows/stand-alone-attributes.md)<br/>
[import](../windows/import.md)<br/>
[importidl](../windows/importidl.md)<br/>
[include](../windows/include-cpp.md)<br/>
[includelib](../windows/includelib-cpp.md)