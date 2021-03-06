---
title: lastprivate |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: reference
f1_keywords:
- lastprivate
dev_langs:
- C++
helpviewer_keywords:
- lastprivate OpenMP clause
ms.assetid: 6ef87b31-375a-47e8-8d0d-281be45fb56a
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 7124e51b604a55d049be13d3bbcccc4e5810ca67
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/19/2018
ms.locfileid: "46412829"
---
# <a name="lastprivate"></a>lastprivate

指定变量在封闭上下文版本将设置为专用版本的任何线程执行的最后一次迭代 （for 循环构造） 或最后一个部分 （#pragma 节）。

## <a name="syntax"></a>语法

```
lastprivate(var)
```

### <a name="parameters"></a>参数

*var*<br/>
设置为等于私有版本的任何线程的变量执行的最后一次迭代 （for 循环构造） 或最后一个部分 （#pragma 节）。

## <a name="remarks"></a>备注

`lastprivate` 适用于以下指令：

- [for](../../../parallel/openmp/reference/for-openmp.md)

- [部分](../../../parallel/openmp/reference/sections-openmp.md)

有关详细信息，请参阅[2.7.2.3 lastprivate](../../../parallel/openmp/2-7-2-3-lastprivate.md)。

## <a name="example"></a>示例

请参阅[计划](../../../parallel/openmp/reference/schedule.md)有关的使用示例`lastprivate`子句。

## <a name="see-also"></a>请参阅

[子句](../../../parallel/openmp/reference/openmp-clauses.md)