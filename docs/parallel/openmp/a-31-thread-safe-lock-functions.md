---
title: A.31 线程安全的锁函数 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 3ad89eb8-076c-405a-be5e-88d3d707a832
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: c25e88b115cb1f82268040a8d17e0dc9eaed3fee
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/19/2018
ms.locfileid: "46408957"
---
# <a name="a31---thread-safe-lock-functions"></a>A.31   线程安全的锁函数

下面的 c + + 示例演示如何通过使用初始化数组的并行区域中的锁`omp_init_lock`([部分 3.2.1](../../parallel/openmp/3-2-1-omp-init-lock-and-omp-init-nest-lock-functions.md) 42 页上)。

## <a name="example"></a>示例

### <a name="code"></a>代码

```
// A_13_omp_init_lock.cpp
// compile with: /openmp
#include <omp.h>

omp_lock_t *new_locks() {
   int i;
   omp_lock_t *lock = new omp_lock_t[1000];
   #pragma omp parallel for private(i)
   for (i = 0 ; i < 1000 ; i++)
      omp_init_lock(&lock[i]);

   return lock;
}

int main () {}
```