---
title: 定义和声明 (C) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
dev_langs:
- C++
helpviewer_keywords:
- export functions
ms.assetid: d150395a-89d4-4298-9ac4-08f84fe1261c
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: d44a98fee82e41252b27fa5a1605b04a15af9115
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2018
ms.locfileid: "32383480"
---
# <a name="definitions-and-declarations-c"></a>定义和声明 (C)
**Microsoft 专用**  
  
 DLL 接口引用已知由此系统中的某个程序导出的所有项（函数和数据）；即，声明为 dllimport 或 `dllexport` 的所有项。 DLL 接口中包含的所有声明必须指定 dllimport 或 `dllexport` 特性。 但是，定义仅可指定 `dllexport` 特性。 例如，以下函数定义产生了一个编译器错误：  
  
```  
#define DllImport   __declspec( dllimport )  
#define DllExport   __declspec( dllexport )  
  
DllImport int func()    /* Error; dllimport prohibited in */  
                        /* definition. */  
{  
   return 1;  
}  
```  
  
 以下代码也会产生错误：  
  
```  
#define DllImport   __declspec( dllimport )  
#define DllExport   __declspec( dllexport )  
  
DllImport int i = 10;      /* Error; this is a definition. */  
```  
  
 但是，这是正确的语法：  
  
```  
#define DllImport   __declspec( dllimport )  
#define DllExport   __declspec( dllexport )  
  
DllExport int i = 10;      /* Okay: this is an export definition. */  
```  
  
 使用 `dllexport` 表示定义，而使用 dllimport 表示声明。 必须使用带 `extern` 的 `dllexport` 关键字来强制进行声明；否则，会进行隐式定义。  
  
```  
#define DllImport   __declspec( dllimport )  
#define DllExport   __declspec( dllexport )  
  
extern DllImport int k;   /* These are correct and imply */  
Dllimport int j;          /* a declaration. */      
```  
  
 **结束 Microsoft 专用**  
  
## <a name="see-also"></a>请参阅  
 [DLL 导入和导出函数](../c-language/dll-import-and-export-functions.md)