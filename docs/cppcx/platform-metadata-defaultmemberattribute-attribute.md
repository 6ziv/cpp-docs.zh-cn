---
title: Platform::Metadata::DefaultMemberAttribute 属性 |Microsoft Docs
ms.custom: ''
ms.date: 12/30/2016
ms.technology: cpp-windows
ms.topic: reference
f1_keywords:
- VCCORLIB/Platform::Metadata::DefaultMemberAttribute
dev_langs:
- C++
helpviewer_keywords:
- Platform::Metadata::DefaultMemberAttribute Attribute
ms.assetid: d8abda01-c257-4371-aec4-541d4825e0af
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 54959b293752ac0453ba383f86ab225e0b45e471
ms.sourcegitcommit: 761c5f7c506915f5a62ef3847714f43e9b815352
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2018
ms.locfileid: "44106987"
---
# <a name="platformmetadatadefaultmemberattribute-attribute"></a>Platform::Metadata::DefaultMemberAttribute 特性

指示首选函数以在几个可能的重载函数中调用。

## <a name="syntax"></a>语法

```cpp
public ref class DefaultMember abstract : Attribute
```

## <a name="inheritance"></a>继承

[Platform::Object](../cppcx/platform-object-class.md)

[Platform::Metadata::Attribute](../cppcx/platform-metadata-attribute-attribute.md)

### <a name="remarks"></a>备注

将 DefaultMember 特性应用于将由 JavaScript 应用程序使用的方法。

### <a name="requirements"></a>要求

**支持的最低客户端：** Windows 8

**支持的最低服务器：** Windows Server 2012

**命名空间：** Platform::Metadata

**元数据：** platform.winmd

## <a name="see-also"></a>请参阅

[Platform::Metadata 命名空间](../cppcx/platform-metadata-namespace.md)