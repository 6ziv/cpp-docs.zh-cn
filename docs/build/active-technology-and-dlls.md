---
title: Active 技术和 Dll |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- in-process server DLLs
- Automation [C++], DLLs
- DLLs [C++], Active Technology
- Active technology [C++]
- MFC DLLs [C++], Active Technology
ms.assetid: 3ed27f8d-164a-4562-ad61-9f2333404cc7
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: efa9a5cf17a4578fc7be9cbadc51605ee32c1650
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/17/2018
ms.locfileid: "45706246"
---
# <a name="active-technology-and-dlls"></a>Active 技术和 DLL

Active 技术使对象服务器得以在 DLL 内完全实现。 此类服务器称为进程内服务器。 MFC 不完全支持进程内服务器的可视化编辑的所有功能主要是因为 Active 技术不提供服务器挂接到容器的主消息循环的一种方法。 MFC 需要访问容器应用程序的消息循环来处理加速键和空闲处理。

如果你正在编写自动化服务器和你的服务器具有的用户界面，可以使您的服务器成为进程内服务器并将其完全置于 DLL。

## <a name="what-do-you-want-to-know-more-about"></a>你想进一步了解什么？

- [自动化服务器](../mfc/automation-servers.md)

## <a name="see-also"></a>请参阅

[Visual C++ 中的 DLL](../build/dlls-in-visual-cpp.md)