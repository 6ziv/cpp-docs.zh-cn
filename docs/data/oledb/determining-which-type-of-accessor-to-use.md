---
title: 确定要使用的访问器的类型 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-data
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- rowsets [C++], data types
- accessors [C++], types
ms.assetid: 22483dd2-f4e0-4dcb-8e4d-cd43a9c1a3db
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 720a72406bec5672757c1b2c5713586b7fc7f1ca
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2018
ms.locfileid: "46086962"
---
# <a name="determining-which-type-of-accessor-to-use"></a>确定要使用的访问器类型

在编译时或在运行时，您可以确定行集上的数据类型。  
  
如果您需要在编译时确定数据类型，使用静态访问器 (如`CAccessor`)。 手动或使用 ATL OLE DB 使用者向导，您可以确定数据类型。  
  
如果您需要在运行时确定的数据类型，使用动态 (`CDynamicAccessor`或其子级) 或手动访问器 (`CManualAccessor`)。 在这些情况下，您可以调用`GetColumnInfo`上要返回的列绑定信息，您可以确定类型的行集。  
  
下表列出了使用者模板中提供的访问器的类型。 每个访问器都有优点和缺点。 具体取决于您的具体情况，一个取值函数类型应满足你的需求。  
  
|访问器类|绑定|参数|注释|  
|--------------------|-------------|---------------|-------------|  
|`CAccessor`|COLUMN_ENTRY 宏创建的用户记录。 宏将该记录中的数据成员绑定到的访问器。 创建行集时，不能为未绑定列。|是的通过使用 PARAM_MAP 宏项。 绑定后，参数不能为未绑定。|由于少量的代码的最快访问器。|  
|`CDynamicAccessor`|自动。|不是。|如果不知道的行集中的数据类型，这很有用。|  
|`CDynamicParameterAccessor`|自动进行的但可以是[重写](../../data/oledb/overriding-a-dynamic-accessor.md)。|是的如果提供程序支持`ICommandWithParameters`。 自动绑定参数。|低于`CDynamicAccessor`但可用于调用泛型存储的过程。|  
|`CDynamicStringAccessor[A,W]`|自动。|不是。|检索从字符串数据作为数据存储区访问的数据。|  
|`CManualAccessor`|手动使用`AddBindEntry`。|使用手动`AddParameterEntry`。|非常快;参数和列绑定仅一次。 确定要使用数据的类型。 (请参阅[DBVIEWER](https://github.com/Microsoft/VCSamples)示例有关的示例。)需要更多代码`CDynamicAccessor`或`CAccessor`。 而是要直接调用 OLE DB。|  
|`CXMLAccessor`|自动。|不是。|检索从字符串数据作为数据存储区访问的数据，并将其格式化为 XML 标记数据。|  
  
## <a name="see-also"></a>请参阅  

[使用访问器](../../data/oledb/using-accessors.md)