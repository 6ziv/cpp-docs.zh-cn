---
title: 设置注册机构代码 （c + +） 的静态链接 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-atl
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- statically linking to ATL Registrar code
- linking [C++], to ATL Registrar code
ms.assetid: 835f5885-87a6-48fa-91e6-60988ee65538
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 7a66ca33aa95ea6ffd59860cf0a55e51266ef5cb
ms.sourcegitcommit: 92dbc4b9bf82fda96da80846c9cfcdba524035af
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/05/2018
ms.locfileid: "43757693"
---
# <a name="setting-up-a-static-link-to-the-registrar-code-c-only"></a>设置静态链接到的注册机构代码 （c + +）

C + + 客户端可以创建注册机构的代码的静态链接。 静态链接的注册机构的分析器将大约 5 K 添加到发布版本。

若要设置静态链接的最简单方法假定已指定[DECLARE_REGISTRY_RESOURCEID](reference/registry-macros.md#declare_registry_resourceid)对象的声明中。 （这是 ATL 的使用的默认值规范）

### <a name="to-create-a-static-link-using-declareregistryresourceid"></a>若要创建使用 DECLARE_REGISTRY_RESOURCEID 的静态链接

1. 指定[/D](../build/reference/d-preprocessor-definitions.md) `_ATL_STATIC_REGISTRY`而不是 /D **_ATL_DLL**。

2. 重新编译。

## <a name="see-also"></a>请参阅

[注册表组件 （注册器）](../atl/atl-registry-component-registrar.md)

