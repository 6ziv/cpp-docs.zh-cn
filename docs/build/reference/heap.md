---
title: -堆 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- /heap
dev_langs:
- C++
helpviewer_keywords:
- heap allocation, setting heap size
- HEAP editbin option
- -HEAP editbin option
- /HEAP editbin option
ms.assetid: 6ce759b5-75b7-44ff-a5fd-3a83a0ba9a48
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 22698760ba23dc60b64002f0f728bb7a036f6731
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/17/2018
ms.locfileid: "45699811"
---
# <a name="heap"></a>/HEAP

设置堆的大小（以字节为单位）。 此选项仅适用于可执行文件。

```

/HEAP:
reserve[,commit]
```

## <a name="remarks"></a>备注

`reserve` 参数指定虚拟内存中的初始堆分配总量。 默认情况下，堆大小为 1 MB。 [EDITBIN 参考](../../build/reference/editbin-reference.md)调高为指定的值为 4 个字节的最接近倍数。

可选`commit`参数是取决于操作系统的解释。 在 Windows 操作系统中，它指定最初要分配的物理内存量和在展开堆时要分配的额外内存量。 提交的虚拟内存后，在分页文件为保留的空间。 当应用需要更多堆空间但又会增加内存需求和可能的应用启动持续时间时，提高 `commit` 值可减少系统分配的内存。 `commit` 值必须小于或等于 `reserve` 值。

以十进制或 C 语言十六进制/八进制表示形式指定 `reserve` 和 `commit` 值。 例如，值 1 MB 可指定为十进制的 1048576、十六进制的 0x100000 或八进制的 04000000。

## <a name="see-also"></a>请参阅

[EDITBIN 选项](../../build/reference/editbin-options.md)