---
title: 'Mutex:: operator = 运算符 |Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::Mutex::operator=
dev_langs:
- C++
helpviewer_keywords:
- operator= operator
ms.assetid: 9b0ee206-a930-4fea-8dc0-1f79839e9d13
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: ea5aee6f248487097462028a763a98b4e814a17a
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/19/2018
ms.locfileid: "46396787"
---
# <a name="mutexoperator-operator"></a>Mutex::operator= 运算符

分配 （移动） 指定**Mutex**对象与当前**互斥体**对象。

## <a name="syntax"></a>语法

```cpp
Mutex& operator=(
   _Inout_ Mutex&& h
);
```

### <a name="parameters"></a>参数

*h*<br/>
对的右值引用**互斥体**对象。

## <a name="return-value"></a>返回值

对当前的引用**互斥体**对象。

## <a name="remarks"></a>备注

有关详细信息，请参阅**移动语义**一部分[右值引用声明符： & &](../cpp/rvalue-reference-declarator-amp-amp.md)。

## <a name="requirements"></a>要求

**标头：** corewrappers.h

**Namespace:** Microsoft::WRL::Wrappers

## <a name="see-also"></a>请参阅

[Mutex 类](../windows/mutex-class1.md)