---
title: CancelTransitionPolicy 枚举 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- module/Microsoft::WRL::CancelTransitionPolicy::TransitionFromCanceled
- module/Microsoft::WRL::CancelTransitionPolicy::RemainCanceled
- module/Microsoft::WRL::CancelTransitionPolicy
dev_langs:
- C++
helpviewer_keywords:
- CancelTransitionPolicy Enumeration
ms.assetid: 5de49f7d-e5e3-43e9-bbca-666caf226cef
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: abc49a62e1cc9fb4abdc56b329b8fa057edebde7
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2018
ms.locfileid: "42583512"
---
# <a name="canceltransitionpolicy-enumeration"></a>CancelTransitionPolicy 枚举

指示异步操作的尝试转换到的终端状态的方式完成或错误的行为根据客户端请求已取消状态。

## <a name="syntax"></a>语法

```cpp
enum CancelTransitionPolicy;
```

## <a name="members"></a>成员

### <a name="values"></a>值

|名称|描述|
|----------|-----------------|
|`RemainCanceled`|如果异步操作目前在客户端请求已取消状态，则表明它将处于已取消状态而不是转换为已完成的终端或错误状态。|
|`TransitionFromCanceled`|如果异步操作目前在客户端请求已取消状态，则表明状态应转换到的终端状态的已取消的状态完成的或由使用此标志的调用确定的错误。|

## <a name="requirements"></a>要求

**标头：** async.h

**命名空间：** Microsoft::WRL

## <a name="see-also"></a>请参阅

[Microsoft::WRL Namespace](../windows/microsoft-wrl-namespace.md)