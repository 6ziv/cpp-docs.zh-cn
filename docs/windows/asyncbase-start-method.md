---
title: 'Asyncbase:: Start 方法 |Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- async/Microsoft::WRL::AsyncBase::Start
dev_langs:
- C++
helpviewer_keywords:
- Start method
ms.assetid: 67405c9d-0d1a-4c1e-8ea4-6ba01c1f90d9
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: d81a3f29e99f49b03eb76f44af60c42d433e0bdc
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2018
ms.locfileid: "42611227"
---
# <a name="asyncbasestart-method"></a>AsyncBase::Start 方法

启动异步操作。

## <a name="syntax"></a>语法

```cpp
STDMETHOD(
   Start
)(void);
```

## <a name="return-value"></a>返回值

如果该操作启动或已，启动，则为 S_OK;否则为 E_ILLEGAL_STATE_CHANGE。

## <a name="remarks"></a>备注

**Start （)** 是默认实现`IAsyncInfo::Start`，并不执行任何实际工作。 若要实际启动异步操作，重写`OnStart()`纯虚方法。

## <a name="requirements"></a>要求

**标头：** async.h

**命名空间：** Microsoft::WRL

## <a name="see-also"></a>请参阅

[AsyncBase 类](../windows/asyncbase-class.md)