---
title: SafeGreaterThan |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- SafeGreaterThan
dev_langs:
- C++
helpviewer_keywords:
- SafeGreaterThan function
ms.assetid: 32cecac9-ba88-43eb-a7a4-30e390456739
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: eab7af0a5a72c8f5b08e046a527026e77ca67dea
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/19/2018
ms.locfileid: "46411451"
---
# <a name="safegreaterthan"></a>SafeGreaterThan

比较两个数字。

## <a name="syntax"></a>语法

```cpp
template<typename T, typename U>
inline bool SafeGreaterThan (
   const T t,
   const U u
) throw ();
```

### <a name="parameters"></a>参数

*t*<br/>
[in]要比较的第一个数字。 其类型必须为`T`。

*u*<br/>
[in]要比较的第二个数字。 其类型必须为`U`。

## <a name="return-value"></a>返回值

**true**如果*t*大于*u*; 否则为**false**。

## <a name="remarks"></a>备注

**SafeGreaterThan**扩展的常规比较运算符，通过它可以比较两个不同类型的数字。

此方法属于[SafeInt 库](../windows/safeint-library.md)，而无需创建的实例的适用的单一比较[SafeInt 类](../windows/safeint-class.md)。

> [!NOTE]
> 此方法仅应在必须保护单个数学运算时使用。 如果存在多个运算，则应使用 `SafeInt` 类而不是调用各个独立函数。

有关模板类型的详细信息`T`并`U`，请参阅[SafeInt 函数](../windows/safeint-functions.md)。

## <a name="requirements"></a>要求

**标头：** safeint.h

**Namespace:** microsoft:: utilities

## <a name="see-also"></a>请参阅

[SafeInt 函数](../windows/safeint-functions.md)<br/>
[SafeInt 库](../windows/safeint-library.md)<br/>
[SafeInt 类](../windows/safeint-class.md)<br/>
[SafeLessThan](../windows/safelessthan.md)<br/>
[SafeLessThanEquals](../windows/safelessthanequals.md)<br/>
[SafeGreaterThanEquals](../windows/safegreaterthanequals.md)