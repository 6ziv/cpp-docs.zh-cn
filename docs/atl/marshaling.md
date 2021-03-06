---
title: 封送处理 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-atl
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- marshaling, COM interop
- marshaling
- COM interfaces, marshaling
ms.assetid: 40644b0a-1106-4fc8-9dfb-9bee9915d825
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 69f1b7e131b614aa4714f0c2be19fab79982031c
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2018
ms.locfileid: "46108613"
---
# <a name="marshaling"></a>封送处理

封送处理的 COM 方法允许在一个进程可以在另一个过程中使用某个对象公开的接口。 在封送处理，COM 提供了代码 （或使用提供的接口实现器代码） 打包到跨进程 （以及在网络上其他计算机运行的进程） 可以移动的格式的方法的参数，并将这些参数解压缩在另一端。 同样，COM 必须执行上述相同步骤，在从调用返回。

> [!NOTE]
>  封送处理时通常不需要与对象相同的进程中正在使用提供的对象的接口。 但是，封送处理可能需要在线程之间。

## <a name="see-also"></a>请参阅

[COM 简介](../atl/introduction-to-com.md)<br/>
[封送处理的详细信息](/windows/desktop/com/marshaling-details)

