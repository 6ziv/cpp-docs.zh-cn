---
title: 'Asyncbase:: Cancel 方法 |Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- async/Microsoft::WRL::AsyncBase::Cancel
dev_langs:
- C++
helpviewer_keywords:
- Cancel method
ms.assetid: 8bfebc63-3848-4629-bc89-aa538ed7e7ad
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: dbf216d672dd22e453f8c213f7a9f34f08a47273
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2018
ms.locfileid: "42593132"
---
# <a name="asyncbasecancel-method"></a>AsyncBase::Cancel 方法

取消异步操作。

## <a name="syntax"></a>语法

```cpp
STDMETHOD(
   Cancel
)(void);
```

## <a name="return-value"></a>返回值

默认情况下，始终返回 S_OK。

## <a name="remarks"></a>备注

**Cancel （)** 是默认实现`IAsyncInfo::Cancel`，并不执行任何实际工作。 若要实际取消异步操作，请重写`OnCancel()`纯虚方法。

## <a name="requirements"></a>要求

**标头：** async.h

**命名空间：** Microsoft::WRL

## <a name="see-also"></a>请参阅

[AsyncBase 类](../windows/asyncbase-class.md)