---
title: 针对旧代码 （Visual c + +） 的浮点支持 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: a2a26b96-7bc2-418a-981a-51aa1a0294a2
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 7285325bf1a934afcef337da318d019ec6fe375c
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/17/2018
ms.locfileid: "45706805"
---
# <a name="floating-point-support-for-older-code-visual-c"></a>针对旧代码的浮点支持 (Visual C++)

MMX 和浮点堆栈寄存器 (MM0-MM7/ST0-ST7) 会保留在上下文切换。  没有这些寄存器显式调用约定。  使用这些寄存器严格禁止在内核模式代码。

## <a name="see-also"></a>请参阅

[调用约定](../build/calling-convention.md)