---
title: 添加另一种语言 （c + +） 的版本信息 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: conceptual
f1_keywords:
- vc.editors.version
dev_langs:
- C++
helpviewer_keywords:
- languages, version information
- New Version Info Block
- blocks, adding
- resources [C++], adding version information
- version information, adding for languages
ms.assetid: 17f6273c-e1cc-441a-a3d8-f564341cbf20
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: bf01f1d4b1c687ed919b94f651ef7ccf4b0bf45d
ms.sourcegitcommit: f0c90000125a9497bf61e41624de189a043703c0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/10/2018
ms.locfileid: "44313439"
---
# <a name="adding-version-information-for-another-language-c"></a>添加另一种语言 （c + +） 的版本信息

### <a name="to-add-version-information-for-another-language-new-info-block"></a>添加其他语言的版本信息（新版本信息块）

1. 通过在 [资源视图](../windows/resource-view-window.md)中双击鼠标打开版本信息资源。

   > [!NOTE]
   > 如果你的项目尚未包含 .rc 文件，请参阅 [创建新的资源脚本文件](../windows/how-to-create-a-resource-script-file.md)。

2. 在版本信息表中单击右键并在快捷菜单中选择“新建版本信息块”  。

   此命令将其他信息块添加到当前版本信息资源，并在 [属性窗口](/visualstudio/ide/reference/properties-window)中打开其相应属性。

3. 在“属性”  窗口中，为新块选择合适的语言和字符集。

有关将资源添加到托管项目的信息，请参阅[桌面应用中的资源](/dotnet/framework/resources/index)中 *.NET Framework 开发人员指南*。 有关手动将资源文件添加到托管项目、 访问资源、 显示静态资源和将资源字符串分配给属性的信息，请参阅[桌面应用中创建资源文件](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)。 全球化和本地化的托管应用中的资源的信息，请参阅[Globalizing and Localizing.NET Framework Applications](/dotnet/standard/globalization-localization/index)。

## <a name="requirements"></a>要求

Win32

## <a name="see-also"></a>请参阅

[版本信息编辑器](../windows/version-information-editor.md)  
[版本信息 (Windows)](https://msdn.microsoft.com/library/windows/desktop/ms646981.aspx)