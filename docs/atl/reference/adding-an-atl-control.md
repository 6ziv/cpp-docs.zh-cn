---
title: 添加 ATL 控件 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-atl
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- ATL projects, adding controls
- controls [ATL], adding to projects
ms.assetid: 10223e7e-fdb7-4163-80c6-44aeafa8e6ce
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 47bbd73efc13eb28ed177c39366ae58cd9c91adc
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2018
ms.locfileid: "46063185"
---
# <a name="adding-an-atl-control"></a>添加 ATL 控件

使用此向导将用户界面对象添加到所有潜在容器支持接口的项目。 若要支持这些接口，该项目必须已创建为 ATL 应用程序或作为包含 ATL 支持的 MFC 应用程序。 可使用 [ATL 项目向导](../../atl/reference/atl-project-wizard.md)创建 ATL 应用程序，或[将 ATL 对象添加到 MFC 应用程序](../../mfc/reference/adding-atl-support-to-your-mfc-project.md)以实现 MFC 应用程序的 ATL 支持。

### <a name="to-add-an-atl-control-to-your-project"></a>若要向项目添加 ATL 控件

1. 在上述**解决方案资源管理器**或[类视图](/visualstudio/ide/viewing-the-structure-of-code)，右键单击你想要添加的 ATL 简单对象的项目的名称。

2. 单击**外**从快捷菜单，然后单击**添加类**。

3. 在中[添加类](../../ide/add-class-dialog-box.md)对话框中，在模板窗格中，单击**ATL 控件**，然后单击**添加**以显示[ATL 控件向导](../../atl/reference/atl-control-wizard.md)。

使用**ATL 控件向导**，可以创建一个三种类型的控件：

- 标准控件

- 复合控件

- DHTML 控件

此外，可以降低控件的大小和删除未使用的大多数容器通过选择接口**最低限度的控制**上**选项**向导页。

## <a name="see-also"></a>请参阅

[向复合控件添加功能](../../atl/adding-functionality-to-the-composite-control.md)<br/>
[ATL COM 对象基础知识](../../atl/fundamentals-of-atl-com-objects.md)   

