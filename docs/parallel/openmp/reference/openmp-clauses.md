---
title: OpenMP 子句 |Microsoft 文档
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: reference
dev_langs:
- C++
ms.assetid: 806e7d8f-b204-4e4c-a12c-273ab540a7ca
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 7abe5a637a2a32c696f19f5ab9988f1be361f647
ms.sourcegitcommit: 7019081488f68abdd5b2935a3b36e2a5e8c571f8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2018
ms.locfileid: "33692833"
---
# <a name="openmp-clauses"></a>OpenMP 子句
提供指向 OpenMP API 中使用的子句。  
  
 Visual c + + 支持以下 OpenMP 子句：  
  
|子句|描述|  
|------------|-----------------|  
|[copyin](../../../parallel/openmp/reference/copyin.md)|允许访问主线程的值的线程[threadprivate](../../../parallel/openmp/reference/threadprivate.md)变量。|  
|[copyprivate](../../../parallel/openmp/reference/copyprivate.md)|将指定应所有线程间共享一个或多个变量。|  
|[default](../../../parallel/openmp/reference/default-openmp.md)|并行区域中指定的未区分范围的变量的行为。|  
|[firstprivate](../../../parallel/openmp/reference/firstprivate.md)|指定每个线程都应具有自己的变量中，实例和变量应用变量的值进行初始化，因为它在并行构造之前已存在。|  
|[if](../../../parallel/openmp/reference/if-openmp.md)|指定是否应在并行或序列中执行循环。|  
|[lastprivate](../../../parallel/openmp/reference/lastprivate.md)|指定的变量的封闭上下文的版本被设置为私有版本的任何线程执行的最后一个迭代 （for 循环构造） 或最后一节 （#pragma 节）。|  
|[nowait](../../../parallel/openmp/reference/nowait.md)|重写指令中隐式屏障。|  
|[num_threads](../../../parallel/openmp/reference/num-threads.md)|在线程团队设置线程的数。|  
|[排序](../../../parallel/openmp/reference/ordered-openmp-clauses.md)|上一个并行需要[为](../../../parallel/openmp/reference/for-openmp.md)语句如果[排序](../../../parallel/openmp/reference/ordered-openmp-directives.md)指令是在循环中使用。|  
|[private](../../../parallel/openmp/reference/private-openmp.md)|指定每个线程都应具有其自己的变量的实例。|  
|[reduction](../../../parallel/openmp/reference/reduction.md)|指定对每个线程都是私有的一个或多个变量是并行区域末尾缩减操作的主题。|  
|[schedule](../../../parallel/openmp/reference/schedule.md)|适用于[为](../../../parallel/openmp/reference/for-openmp.md)指令。|  
|[shared](../../../parallel/openmp/reference/shared-openmp.md)|将指定应所有线程间共享一个或多个变量。|  
  
## <a name="see-also"></a>请参阅  
 [OpenMP](../../../parallel/openmp/openmp-in-visual-cpp.md)   
 [指令](../../../parallel/openmp/reference/openmp-directives.md)