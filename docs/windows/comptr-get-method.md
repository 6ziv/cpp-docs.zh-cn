---
title: 'Comptr:: Get 方法 |Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- client/Microsoft::WRL::ComPtr::Get
dev_langs:
- C++
helpviewer_keywords:
- Get method
ms.assetid: 078eee51-7bca-4924-a74b-cd4f6a05de31
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: ca996b7893fd19076504fd91bbb5e80bbe692883
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2018
ms.locfileid: "42608659"
---
# <a name="comptrget-method"></a>ComPtr::Get 方法

检索指向与此相关联的接口**ComPtr**。

## <a name="syntax"></a>语法

```cpp
T* Get() const;
```

## <a name="return-value"></a>返回值

指向与此相关联的接口指针**ComPtr**。

## <a name="requirements"></a>要求

**标头：** client.h

**命名空间：** Microsoft::WRL

## <a name="see-also"></a>请参阅

[ComPtr 类](../windows/comptr-class.md)