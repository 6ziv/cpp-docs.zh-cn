---
title: CompareStringOrdinal 方法 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::Details::CompareStringOrdinal
dev_langs:
- C++
ms.assetid: ffa997fd-8cd7-40a5-b9e7-f55d40b072f4
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 952de0ca136d29eb0b170856410b18a1d65120c1
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2018
ms.locfileid: "42612883"
---
# <a name="comparestringordinal-method"></a>CompareStringOrdinal 方法

支持 WRL 基础结构，不应在代码中直接使用。

## <a name="syntax"></a>语法

```cpp
inline INT32 CompareStringOrdinal(
   HSTRING lhs,
   HSTRING rhs)  
```

### <a name="parameters"></a>参数

*lhs*  
第一个要比较的 HSTRING。

*rhs*  
要比较的第二个 HSTRING。

## <a name="return-value"></a>返回值

|“值”|条件|
|-----------|---------------|
|-1|*lhs*是小于*rhs*。|
|0|*lhs*等于*rhs*。|
|1|*lhs*大于*rhs*。|

## <a name="remarks"></a>备注

比较两个指定的 HSTRING 对象并返回一个整数，指示二者在排序顺序中的相对位置。

## <a name="requirements"></a>要求

**标头：** corewrappers.h

**Namespace:** Microsoft::WRL::Wrappers::Details

## <a name="see-also"></a>请参阅

[Microsoft::WRL::Wrappers::Details 命名空间](../windows/microsoft-wrl-wrappers-details-namespace.md)