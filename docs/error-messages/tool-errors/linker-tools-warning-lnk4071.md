---
title: 链接器工具警告 LNK4071 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- LNK4071
dev_langs:
- C++
helpviewer_keywords:
- LNK4071
ms.assetid: 803f8c34-8219-4f55-a4ae-7133ceff2ba3
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d11247c823a93604359b4cab6995b694bcf5a2f3
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2018
ms.locfileid: "46064658"
---
# <a name="linker-tools-warning-lnk4071"></a>链接器工具警告 LNK4071

不能以增量方式链接后面的链接上

找到多个定义的一个或多个符号链接，但[/force](../../build/reference/force-force-file-output.md)或 **/FORCE:MULTIPLE**用于创建输出文件而不考虑错误。 删除链接的增量状态 (.ilk) 文件。