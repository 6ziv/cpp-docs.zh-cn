---
title: 'Hstringreference:: Operator = 运算符 |Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::HStringReference::operator=
dev_langs:
- C++
ms.assetid: ea100ed3-e566-4c9e-b6a8-f296088dea9c
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 933d332ce2653fd8ea907a5fafda524ae0220906
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/19/2018
ms.locfileid: "46408994"
---
# <a name="hstringreferenceoperator-operator"></a>HStringReference::Operator= 运算符

另一个的值移**HStringReference**对象与当前**HStringReference**对象。

## <a name="syntax"></a>语法

```cpp
HStringReference& operator=(HStringReference&& other) throw()  
```

### <a name="parameters"></a>参数

*other*<br/>
将现有**HStringReference**对象。

## <a name="remarks"></a>备注

现有值*其他*对象复制到当前**HStringReference**对象，然后*其他*对象被销毁。

## <a name="requirements"></a>要求

**标头：** corewrappers.h

**Namespace:** Microsoft::WRL::Wrappers

## <a name="see-also"></a>请参阅

[HStringReference 类](../windows/hstringreference-class.md)