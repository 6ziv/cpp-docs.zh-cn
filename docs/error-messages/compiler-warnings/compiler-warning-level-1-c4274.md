---
title: 编译器警告 （等级 1） C4274 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4274
dev_langs:
- C++
helpviewer_keywords:
- C4274
ms.assetid: 5a948680-7ed1-469f-978d-ae99d154e161
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 5f6db0ee96674beda51ab02c8651e6f4960a0bf8
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2018
ms.locfileid: "46094677"
---
# <a name="compiler-warning-level-1-c4274"></a>编译器警告 （等级 1） C4274

\#ident 忽略;请参阅 #pragma comment （exestr，'string'） 的文档

`#ident`指令，插入用户指定的字符串对象或可执行文件中，已弃用。 因此，编译器会忽略该指令。

> [!CAUTION]
>  警告 C4274 建议您在使用[#pragma comment （exestr，'string'）](../../preprocessor/comment-c-cpp.md)指令。 但是，这一建议已弃用，将在未来版本的编译器中进行了修订。 如果您使用`#pragma`指令，链接器工具 (LINK.exe) 将忽略注释记录生成的指令并发出警告[LNK4229](../../error-messages/tool-errors/linker-tools-warning-lnk4229.md)。 而不是`#ident`指令，我们建议在你的应用程序中使用的文件版本资源字符串。

## <a name="to-correct-this-error"></a>更正此错误

- 删除`#ident "`*字符串*`"`指令。

## <a name="see-also"></a>请参阅

[注释 (C/C++)](../../preprocessor/comment-c-cpp.md)<br/>
[链接器工具警告 LNK4229](../../error-messages/tool-errors/linker-tools-warning-lnk4229.md)<br/>
[使用资源文件](../../windows/working-with-resource-files.md)