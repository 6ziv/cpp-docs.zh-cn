---
title: 'Module:: module 构造函数 |Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- module/Microsoft::WRL::Module::Module
dev_langs:
- C++
helpviewer_keywords:
- Module, constructor
ms.assetid: 5436fc74-61dc-41b6-81af-4f03177159aa
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: e96e6cf984196cbca3051eec397ae06e48e2f1c0
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/19/2018
ms.locfileid: "46406654"
---
# <a name="modulemodule-constructor"></a>Module::Module 构造函数

初始化的新实例**模块**类。

## <a name="syntax"></a>语法

```cpp
Module();
```

## <a name="remarks"></a>备注

此构造函数受到保护，不能调用带有**新**关键字。 请调用[module:: getmodule 方法](../windows/module-getmodule-method.md)或[module:: create 方法](../windows/module-create-method.md)。

## <a name="requirements"></a>要求

**标头：** module.h

**命名空间：** Microsoft::WRL

## <a name="see-also"></a>请参阅

[Module 类](../windows/module-class.md)