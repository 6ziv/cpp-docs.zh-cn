---
title: 'Chaininterfaces:: Verify 方法 |Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- implements/Microsoft::WRL::ChainInterfaces::Verify
dev_langs:
- C++
helpviewer_keywords:
- Verify method
ms.assetid: c591e130-8686-4130-ba69-1aaedc250038
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: e6dbc595714cbecf2ad13db13051866e31e5ebcd
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2018
ms.locfileid: "42581053"
---
# <a name="chaininterfacesverify-method"></a>ChainInterfaces::Verify 方法

验证每个接口定义的模板参数*I0*通过*I9*继承`IUnknown`和/或`IInspectable`，以及*I0*继承*I1*通过*I9*。

## <a name="syntax"></a>语法

```cpp
WRL_NOTHROW __forceinline static void Verify();
```

## <a name="remarks"></a>备注

如果验证操作失败， **static_assert**发出描述失败的错误消息。

模板参数*I0*并*I1*是必需的并且参数*I2*通过*I9*都是可选的。

## <a name="requirements"></a>要求

**标头：** implements.h

**命名空间：** Microsoft::WRL

## <a name="see-also"></a>请参阅

[ChainInterfaces 结构](../windows/chaininterfaces-structure.md)