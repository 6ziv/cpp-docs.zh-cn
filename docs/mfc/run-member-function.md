---
title: 运行成员函数 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- WinMain method [MFC]
ms.assetid: 24ab7597-2354-495b-9a20-2c8ccc7385b3
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 446b1b6fc2a5265e2c4eb8a608ff8b4f0028c57d
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/19/2018
ms.locfileid: "46408227"
---
# <a name="run-member-function"></a>运行成员函数

Framework 应用程序需要花大部分时间[运行](../mfc/reference/cwinapp-class.md#run)类的成员函数[CWinApp](../mfc/reference/cwinapp-class.md)。 初始化后`WinMain`调用`Run`来处理消息循环。

`Run` 依次切换程序消息循环，检查有可用消息的消息队列。 如果一条消息可用，`Run`调度的操作。 如果没有消息可用，这是通常为 true，`Run`调用`OnIdle`执行您或框架可能需要完成任何空闲时间处理。 如果没有要执行的消息和空闲处理，则应用程序将进行等待，直到发生某些情况。 当应用程序终止时，`Run`调用`ExitInstance`。 在图[OnIdle 成员函数](../mfc/onidle-member-function.md)消息循环中显示的操作序列。

消息调度取决于消息类型。 有关详细信息，请参阅[消息和框架中的命令](../mfc/messages-and-commands-in-the-framework.md)。

## <a name="see-also"></a>请参阅

[CWinApp：应用程序类](../mfc/cwinapp-the-application-class.md)
