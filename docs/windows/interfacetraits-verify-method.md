---
title: 'Interfacetraits:: Verify 方法 |Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- implements/Microsoft::WRL::Details::InterfaceTraits::Verify
dev_langs:
- C++
helpviewer_keywords:
- Verify method
ms.assetid: 46edd67f-7952-4552-a157-55e823f616c8
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: e1950d6e9d5195ece315863b664b42411231184d
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/19/2018
ms.locfileid: "46415377"
---
# <a name="interfacetraitsverify-method"></a>InterfaceTraits::Verify 方法

支持 WRL 基础结构，不应在代码中直接使用。

## <a name="syntax"></a>语法

```cpp
__forceinline static void Verify();
```

## <a name="remarks"></a>备注

验证`Base`正确派生。

有关详细信息`Base`，请参阅**公共 Typedef**主题中[InterfaceTraits 结构](../windows/interfacetraits-structure.md)。

## <a name="requirements"></a>要求

**标头：** implements.h

**Namespace:** Microsoft::WRL::Details

## <a name="see-also"></a>请参阅

[InterfaceTraits 结构](../windows/interfacetraits-structure.md)<br/>
[Microsoft::WRL::Details 命名空间](../windows/microsoft-wrl-details-namespace.md)