---
title: C 运行时错误 R6026 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- R6026
dev_langs:
- C++
helpviewer_keywords:
- R6026
ms.assetid: 7ea751f8-fc20-46ab-99ef-84c95ca0b6b4
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 824649a28edc1b630eb2fbacd7beec05d74975a9
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2018
ms.locfileid: "46087419"
---
# <a name="c-runtime-error-r6026"></a>C 运行时错误 R6026

没有足够的空间用于 stdio 初始化

> [!NOTE]
>  如果运行应用时遇到此错误消息，该应用已关闭，因为它具有内部内存问题。 有多种原因引起此错误，但通常由极低内存条件。 它也导致应用程序中的 bug，它使用的 Visual c + + 库损坏或驱动程序。
>
>  可以尝试以下步骤来修复此错误：
>
>  -   关闭其他正在运行的应用程序或重新启动计算机以释放内存。
> -   使用**应用程序和功能**或**程序和功能**页**控制面板**来修复或重新安装该程序。
> -   如果应用已使用另一个应用程序或驱动程序的最近安装之前，使用**应用程序和功能**或**程序和功能**页**控制面板**删除新的应用程序或驱动程序，然后重试您的应用程序。
> -   使用**应用程序和功能**或**程序和功能**页**控制面板**修复或重新安装的 Microsoft Visual c + + 可再发行的所有副本。
> -   检查**Windows Update**中**控制面板**的软件更新。
> -   检查应用程序的更新版本。 如果问题仍然存在，请与应用供应商联系。

**程序员提供的的信息**

当没有足够内存可用来初始化 C 运行时中的标准 I/O 支持时，会发生此错误。 在应用启动时，通常会出现此错误。 验证您的应用程序和驱动程序和加载的 dll 不损坏堆在启动时。