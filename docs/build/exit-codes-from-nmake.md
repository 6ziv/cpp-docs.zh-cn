---
title: 从 NMAKE 退出代码 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- NMAKE program, exit codes
- exit codes
ms.assetid: 75f6913c-1da5-4572-a2d3-8a4e058bed15
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 3b5a593e38efb5230630ed01e65f4bfb1f2ba92a
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/17/2018
ms.locfileid: "45722613"
---
# <a name="exit-codes-from-nmake"></a>从 NMAKE 退出代码

NMAKE 返回以下退出代码：

|代码|含义|
|----------|-------------|
|0|无错误 （可能是警告）|
|1|不完整的生成 （仅在使用 /K 时发出）|
|2|程序错误，可能是由于以下值之一：|
||的在生成文件中语法错误|
||的从命令错误或退出代码|
||-由用户中断|
|4|系统错误-内存不足|
|255|目标不是最新的 （仅在使用 /Q 时发出）|

## <a name="see-also"></a>请参阅

[运行 NMAKE](../build/running-nmake.md)