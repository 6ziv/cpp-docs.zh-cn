---
title: 导入 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- vc-attr.import
dev_langs:
- C++
helpviewer_keywords:
- import attribute
ms.assetid: ebf07cae-39fb-4047-8b57-54af0a9a83de
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: a9e2ee577c3285a7e4c3db2fb19d934417bbe26d
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/19/2018
ms.locfileid: "46411555"
---
# <a name="import"></a>import

指定包含要引用主要 IDL 中定义的另一个.idl、.odl 或标头文件。

## <a name="syntax"></a>语法

```cpp
[ import(
   idl_file
) ];
```

### <a name="parameters"></a>参数

*idl_file*<br/>
要导入当前项目的类型库的.idl 文件的名称。

## <a name="remarks"></a>备注

**导入**c + + 属性会导致`#import`语句下面放置`import "docobj.idl"`语句生成的.idl 文件中。 **导入**属性具有相同的功能[导入](/windows/desktop/Midl/import)MIDL 特性。

**导入**属性仅将指定的文件放入你的项目; 将生成的.idl 文件**导入**属性不允许您从源代码中指定的文件调用构造在你的项目。  若要从项目中的源代码在指定的文件中调用的构造，使用[#import](../preprocessor/hash-import-directive-cpp.md)并`embedded_idl`属性也可以将的.h 文件*idl_file*，如果存在的.h 文件。

## <a name="example"></a>示例

下面的代码：

```cpp
// cpp_attr_ref_import.cpp
// compile with: /LD
[module(name="MyLib")];
[import(import.idl)];
```

生成生成的.idl 文件中的以下代码：

```
import "docobj.idl";
import "import.idl";

[ uuid(EED3644C-8488-3ECD-BA97-147DB3CDB499), version(1.0) ]
library MyLib {
   importlib("stdole2.tlb");
   importlib("olepro32.dll");
...
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

[IDL 特性](../windows/idl-attributes.md)<br/>
[独立特性](../windows/stand-alone-attributes.md)<br/>
[importidl](../windows/importidl.md)<br/>
[importlib](../windows/importlib.md)<br/>
[include](../windows/include-cpp.md)<br/>
[includelib](../windows/includelib-cpp.md)  