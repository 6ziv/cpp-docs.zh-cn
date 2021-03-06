---
title: 使用合并模块重新分发组件 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-ide
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- merge modules, using
- redistributing applications, using merge modules
ms.assetid: 93b84211-bf9b-4a78-9f22-474ac2ef7840
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d816d932ce518e006e5537075fe4ac7782362ad4
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/29/2018
ms.locfileid: "43206979"
---
# <a name="redistributing-components-by-using-merge-modules"></a>使用合并模块重新发布组件
Visual Studio 包括获许与应用程序一起重新发布的每个 Visual C++ 组件的[合并模块](/windows/desktop/Msi/about-merge-modules)。 合并模块在 Windows Installer 安装文件中编译后，便可以将特定的 DLL 部署到具有特定平台的计算机。 在你的安装文件中，请指定合并模块是应用程序的先决条件。 Visual Studio 安装后，合并模块将安装在\Program Files\Common Files\Merge Modules\\。 （只能重新发布 Visual C++ DLL 的非调试版本。）有关更多信息以及获许重新发布的合并模块列表的链接，请参阅[重新分发 Visual C++ 文件](../ide/redistributing-visual-cpp-files.md)。  
  
 你可以使用合并模块将可再发行的 Visual C++ DLL 安装到 %SYSTEMROOT%\system32\ 文件夹。 （Visual Studio 本身使用此技术。）但是，安装的用户必须具有管理员权限才能成功安装到该文件夹。  
  
 除非你不必为应用程序提供服务并且不依赖于一个以上的 DLL 版本，否则我们建议你不要使用合并模块。 同一 DLL 的不同版本的合并模块不能包含在一个安装程序中，而且合并模块使你难以独立于应用程序为 DLL 服务。 因而我们建议安装 Visual C++ Redistributable Package。  
  
## <a name="see-also"></a>请参阅  
 [重新分发 Visual C++ 文件](../ide/redistributing-visual-cpp-files.md)