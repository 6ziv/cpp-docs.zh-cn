---
title: MIDL 属性页：常规 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-ide
ms.topic: conceptual
f1_keywords:
- VC.Project.VCMidlTool.PreprocessorDefinitions
- VC.Project.VCMidlTool.DefaultCharType
- VC.Project.VCMidlTool.WarnAsError
- VC.Project.VCMidlTool.AdditionalIncludeDirectories
- VC.Project.VCMidlTool.WarningLevel
- VC.Project.VCMidlTool.MkTypLibCompatible
- VC.Project.VCMidlTool.GenerateStublessProxies
- VC.Project.VCMidlTool.SuppressStartupBanner
- VC.Project.VCMidlTool.TargetEnvironment
- VC.Project.VCMidlTool.OVERWRITEStandardIncludePath
dev_langs:
- C++
helpviewer_keywords:
- MIDL, property pages
ms.assetid: 0692484c-a7e6-4270-8df7-981589368399
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: eae97f795898c97bfb371637fc52a27c9e39039d
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/29/2018
ms.locfileid: "43204684"
---
# <a name="midl-property-pages-general"></a>MIDL 属性页：常规
MIDL 文件夹中的“常规”属性页指定以下 MIDL 编译器选项：  
  
-   预处理器定义 [(/D](https://msdn.microsoft.com/library/windows/desktop/aa367321))  
  
-   附加包含目录 ([/I](https://msdn.microsoft.com/library/windows/desktop/aa367328))  
  
-   忽略标准包含路径 ([/no_def_idir](https://msdn.microsoft.com/library/windows/desktop/aa367347))  
  
-   与 MkTypLib 兼容 ([/mktyplib203](https://msdn.microsoft.com/library/windows/desktop/aa367332))  
  
-   警告等级 ([/W](https://msdn.microsoft.com/library/windows/desktop/aa367383))  
  
-   警告视为错误 ([/WX](https://msdn.microsoft.com/library/windows/desktop/aa367387))  
  
-   取消显示启动版权标志 ([/nologo](https://msdn.microsoft.com/library/windows/desktop/aa367341))  
  
-   MIDL Char 类型 ([/char](https://msdn.microsoft.com/library/windows/desktop/aa367314))  
  
-   目标环境 ([/env](https://msdn.microsoft.com/library/windows/desktop/aa367323))  
  
-   生成无存根(Stub)代理 ([/Oicf](https://msdn.microsoft.com/library/windows/desktop/aa367352))  
  
 有关如何访问 MIDL 文件夹中的“常规”属性页的信息，请参阅[使用项目属性](../ide/working-with-project-properties.md)。  
  
 有关如何以编程方式访问 C++ 项目的 MIDL 选项的信息，请参阅 <xref:Microsoft.VisualStudio.VCProjectEngine.VCMidlTool> 对象。  
  
## <a name="see-also"></a>请参阅  
 [“MIDL”属性页](../ide/midl-property-pages.md)