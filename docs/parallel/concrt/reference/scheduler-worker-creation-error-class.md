---
title: scheduler_worker_creation_error 类 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-concrt
ms.topic: reference
f1_keywords:
- scheduler_worker_creation_error
- CONCRT/concurrency::scheduler_worker_creation_error
- CONCRT/concurrency::scheduler_worker_creation_error::scheduler_worker_creation_error
dev_langs:
- C++
helpviewer_keywords:
- scheduler_worker_creation_error class
ms.assetid: 4aec1c3e-c32a-41b2-899d-2d898f23b3c7
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 3d050ee426817c04518a41b515f30ac348bf7d86
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/19/2018
ms.locfileid: "46400167"
---
# <a name="schedulerworkercreationerror-class"></a>scheduler_worker_creation_error 类

此类描述因未能在并发运行时中创建辅助执行上下文而引发的异常。

## <a name="syntax"></a>语法

```
class scheduler_worker_creation_error : public scheduler_resource_allocation_error;
```

## <a name="members"></a>成员

### <a name="public-constructors"></a>公共构造函数

|名称|描述|
|----------|-----------------|
|[scheduler_worker_creation_error](#ctor)|已重载。 构造 `scheduler_worker_creation_error` 对象。|

## <a name="remarks"></a>备注

该异常通常是在调用并发运行时内创建执行上下文的操作系统失败时引发。 执行上下文是在并发运行时中执行任务的线程。 通常通过调用 Win32 方法 `GetLastError` 返回的错误代码将转换为类型 `HRESULT` 的一个值，并且可以使用基类方法 `get_error_code` 检索。

## <a name="inheritance-hierarchy"></a>继承层次结构

`exception`

[scheduler_resource_allocation_error](scheduler-resource-allocation-error-class.md)

`scheduler_worker_creation_error`

## <a name="requirements"></a>要求

**标头：** concrt.h

**命名空间：** 并发

##  <a name="ctor"></a> scheduler_worker_creation_error

构造 `scheduler_worker_creation_error` 对象。

```
scheduler_worker_creation_error(
    _In_z_ const char* _Message,
    HRESULT _Hresult) throw();

explicit _CRTIMP scheduler_worker_creation_error(
    HRESULT _Hresult) throw();
```

### <a name="parameters"></a>参数

*消息 （_m)*<br/>
错误的描述性消息。

*_Hresult*<br/>
`HRESULT`错误导致异常的值。

## <a name="see-also"></a>请参阅

[并发命名空间](concurrency-namespace.md)
