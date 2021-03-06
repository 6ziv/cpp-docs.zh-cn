---
title: 'Comptrref:: Releaseandgetaddressof 方法 |Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- client/Microsoft::WRL::Details::ComPtrRef::ReleaseAndGetAddressOf
dev_langs:
- C++
helpviewer_keywords:
- ReleaseAndGetAddressOf method
ms.assetid: 004aac42-e135-41ce-8d1d-4c5969d55004
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 03f709feddb1c0e9c82cf80a4bd5f24e531414d3
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2018
ms.locfileid: "42611214"
---
# <a name="comptrrefreleaseandgetaddressof-method"></a>ComPtrRef::ReleaseAndGetAddressOf 方法

支持 WRL 基础结构，不应在代码中直接使用。

## <a name="syntax"></a>语法

```cpp
InterfaceType** ReleaseAndGetAddressOf();
```

## <a name="return-value"></a>返回值

指向表示的接口的已删除**ComPtrRef**对象。

## <a name="remarks"></a>备注

删除当前**ComPtrRef**对象并返回到由表示的接口的指针到-的指针**ComPtrRef**对象。

## <a name="requirements"></a>要求

**标头：** client.h

**Namespace:** Microsoft::WRL::Details

## <a name="see-also"></a>请参阅

[ComPtrRef 类](../windows/comptrref-class.md)  
[Microsoft::WRL::Details 命名空间](../windows/microsoft-wrl-details-namespace.md)