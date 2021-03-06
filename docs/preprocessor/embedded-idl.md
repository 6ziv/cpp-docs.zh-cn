---
title: embedded_idl |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- embedded_idl
dev_langs:
- C++
helpviewer_keywords:
- embedded_idl attribute
ms.assetid: f1c1c2e8-3872-4172-8795-8d1288a20452
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b41af8375249a48ac3a866af224370b19f071d28
ms.sourcegitcommit: d4c803bd3a684d7951bf88dcecf1f14af43ae411
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/10/2018
ms.locfileid: "42539742"
---
# <a name="embeddedidl"></a>embedded_idl
**C + + 专用**  
  
指定将类型库写入保留了特性生成的代码的 .tlh 文件。  
  
## <a name="syntax"></a>语法  
  
```  
embedded_idl[("param")]  
```  
  
### <a name="parameters"></a>参数  
*param*  
可以是以下两个值之一：  
  
- emitidl：从类型库导入的类型信息将出现在为特性化项目生成的 IDL 中。  如果不为 `embedded_idl` 指定参数，则这是默认值，并将有效。  
  
- no_emitidl：从类型库导入的类型信息将不出现在为特性化项目生成的 IDL 中。  
  
## <a name="example"></a>示例  
  
```cpp  
// import_embedded_idl.cpp  
// compile with: /LD  
#include <windows.h>  
[module(name="MyLib2")];  
#import "\school\bin\importlib.tlb" embedded_idl("no_emitidl")  
```  
  
## <a name="remarks"></a>备注  
 
**结束 c + + 专用**  
  
## <a name="see-also"></a>请参阅  
 
[#import 属性](../preprocessor/hash-import-attributes-cpp.md)   
[#import 指令](../preprocessor/hash-import-directive-cpp.md)