---
title: 'Invokehelper:: Invokehelper 构造函数 |Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- event/Microsoft::WRL::Details::InvokeHelper::InvokeHelper
dev_langs:
- C++
helpviewer_keywords:
- InvokeHelper, constructor
ms.assetid: 0223c574-abc3-4fc0-99e6-38626ba79243
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 1ad09a5a4794a9db8882a088f90da5046b6f7b9d
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2018
ms.locfileid: "42609235"
---
# <a name="invokehelperinvokehelper-constructor"></a>InvokeHelper::InvokeHelper 构造函数

支持 WRL 基础结构，不应在代码中直接使用。

## <a name="syntax"></a>语法

```cpp
explicit InvokeHelper(
   TCallback callback
);
```

### <a name="parameters"></a>参数

*回调*  
事件处理程序。

## <a name="remarks"></a>备注

初始化的新实例**InvokeHelper**类。

`TCallback`模板参数指定的事件处理程序的类型。

## <a name="requirements"></a>要求

**标头：** event.h

**Namespace:** Microsoft::WRL::Details

## <a name="see-also"></a>请参阅

[InvokeHelper 结构](../windows/invokehelper-structure.md)  
[Microsoft::WRL::Details 命名空间](../windows/microsoft-wrl-details-namespace.md)