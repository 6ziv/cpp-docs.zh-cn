---
title: 'Dontusenewusemake:: Operator new 运算符 |Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- implements/Microsoft::WRL::Details::DontUseNewUseMake::operator new
dev_langs:
- C++
helpviewer_keywords:
- operator new operator
ms.assetid: 6af07a0d-2271-430c-9d9b-5a4223fed049
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 99e82de06f64816521c47c78648108a9ae815279
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/19/2018
ms.locfileid: "46443223"
---
# <a name="dontusenewusemakeoperator-new-operator"></a>DontUseNewUseMake::operator new 运算符

支持 WRL 基础结构，不应在代码中直接使用。

## <a name="syntax"></a>语法

```cpp
void* operator new(
   size_t,
   _In_ void* placement
);
```

### <a name="parameters"></a>参数

*__unnamed0*<br/>
一个未命名的参数，它指定要分配的内存字节数。

*放置*<br/>
要分配的类型。

## <a name="return-value"></a>返回值

提供了一种方法将传递其他参数，如果重载运算符**新**。

## <a name="remarks"></a>备注

重载运算符**新**，并防止中正在使用`RuntimeClass`。

## <a name="requirements"></a>要求

**标头：** implements.h

**Namespace:** Microsoft::WRL::Details

## <a name="see-also"></a>请参阅

[DontUseNewUseMake 类](../windows/dontusenewusemake-class.md)<br/>
[Microsoft::WRL::Details 命名空间](../windows/microsoft-wrl-details-namespace.md)