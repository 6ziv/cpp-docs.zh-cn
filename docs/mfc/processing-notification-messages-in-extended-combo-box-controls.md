---
title: 处理中的通知消息扩展组合框控件 |Microsoft 文档
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- extended combo boxes [MFC], notifications
- notifications [MFC], extended combo box controls
ms.assetid: 4e442758-d054-4746-bb1a-6ff84accb127
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 576735841748d0b99053d038f8d5f674d5692f00
ms.sourcegitcommit: 060f381fe0807107ec26c18b46d3fcb859d8d2e7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "36930184"
---
# <a name="processing-notification-messages-in-extended-combo-box-controls"></a>处理扩展组合框控件中的通知消息
当用户与扩展组合框进行交互时，控件 (`CComboBoxEx`) 会将通知消息发送到其父窗口（通常是一个视图或对话框对象）。 如果您要在响应中做些什么，请处理这些消息。 例如，当用户激活下拉列表，或单击控件的编辑框中，发送 CBEN_BEGINEDIT 通知。  
  
 请使用“属性”窗口将通知处理程序添加到你希望实现的那些消息的父类。  
  
 下表介绍了由扩展组合框控件发送的各种通知。  
  
-   CBEN_BEGINEDIT 发送用户激活下拉列表或在控件的编辑框中单击时。  
  
-   CBEN_DELETEITEM 发送时已删除了项目。  
  
-   CBEN_DRAGBEGIN 发送当用户开始拖动控件编辑部分中显示的项的图像。  
  
-   CBEN_ENDEDIT 发送用户结束编辑框中的某个操作或从控件的下拉列表中选择某个项时。  
  
-   CBEN_GETDISPINFO 发送，以检索有关回调项的显示信息。  
  
-   CBEN_INSERTITEM 发送时在控件中插入新项。  
  
## <a name="see-also"></a>请参阅  
 [使用 CComboBoxEx](../mfc/using-ccomboboxex.md)   
 [控件](../mfc/controls-mfc.md)

