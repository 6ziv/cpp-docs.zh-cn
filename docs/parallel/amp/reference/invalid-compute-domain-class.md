---
title: invalid_compute_domain 类 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-amp
ms.topic: reference
f1_keywords:
- invalid_compute_domain
- AMPRT/invalid_compute_domain
- AMPRT/Concurrency::invalid_compute_domain::invalid_compute_domain
dev_langs:
- C++
helpviewer_keywords:
- invalid_compute_domain class
ms.assetid: ac7a7166-8bdb-4db1-8caf-ea129ab5117e
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: def102ecb8063f82d90d41b2b678ff22638b1f8b
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2018
ms.locfileid: "46116004"
---
# <a name="invalidcomputedomain-class"></a>invalid_compute_domain 类
当运行时不能通过使用在指定的计算域启动内核时引发的异常[parallel_for_each](concurrency-namespace-functions-amp.md#parallel_for_each)调用站点。  

  
## <a name="syntax"></a>语法  
  
```  
class invalid_compute_domain : public runtime_exception;  
```  
  
## <a name="members"></a>成员  
  
### <a name="public-constructors"></a>公共构造函数  
  
|名称|描述|  
|----------|-----------------|  
|[invalid_compute_domain 构造函数](#ctor)|初始化 `invalid_compute_domain` 类的新实例。|  

  
## <a name="inheritance-hierarchy"></a>继承层次结构  
 `exception`  
  
 `runtime_exception`  
  
 `invalid_compute_domain`  
  
## <a name="requirements"></a>要求  
 **标头：** amprt.h  
  
 **命名空间：** 并发  

## <a name="ctor"></a> invalid_compute_domain 

初始化类的新实例。  
  
## <a name="syntax"></a>语法  
  
```  
explicit invalid_compute_domain(  
    const char * _Message ) throw();  
  
invalid_compute_domain() throw();  
```  
  
### <a name="parameters"></a>参数  
*消息 （_m)*<br/>
错误说明。  
  
### <a name="return-value"></a>返回值  
 实例`invalid_compute_domain`类  
    
## <a name="see-also"></a>请参阅  
 [并发命名空间 (C++ AMP)](concurrency-namespace-cpp-amp.md)
