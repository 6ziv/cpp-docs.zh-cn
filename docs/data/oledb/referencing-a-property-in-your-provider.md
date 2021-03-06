---
title: 您的提供程序中引用属性 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-data
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- OLE DB providers, properties
- references, to properties in providers
- referencing properties in providers
ms.assetid: bfbb3851-5eed-467a-a179-4a97a9515525
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: f6730746cbb3da08e52b5a4d9936aa48a8484886
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2018
ms.locfileid: "46052551"
---
# <a name="referencing-a-property-in-your-provider"></a>在提供程序中引用属性

找到所需的属性的属性组和属性 ID。 有关详细信息，请参阅[OLE DB 属性](/previous-versions/windows/desktop/ms722734\(v=vs.85\))中*OLE DB 程序员参考*。  
  
下面的示例假定你尝试从行集中获取的属性。 使用会话或命令的代码类似，但使用不同的接口。  
  
创建[CDBPropSet](../../data/oledb/cdbpropset-class.md)对象作为构造函数的参数中使用属性组。 例如：  
  
```cpp  
CDBPropSet propset(DBPROPSET_ROWSET);  
```  
  
调用[AddProperty](../../data/oledb/cdbpropset-addproperty.md)，将其传递属性 ID 和要分配给属性的值。 值的类型取决于正在使用的属性。  
  
```cpp  
CDBPropSet propset(DBPROPSET_ROWSET);  

propset.AddProperty(DBPROP_IRowsetChange, true);  

propset.AddProperty(DBPROP_UPDATABILITY, DBPROPVAL_UP_INSERT | DBPROPVAL_UP_CHANGE | DBPROPVAL_UP_DELETE);  
```  
  
使用`IRowset`接口来调用`GetProperties`。 将属性设置作为参数传递。 下面是最终代码：  
  
```cpp  
CAgentRowset<CMyProviderCommand>* pRowset = (CAgentRowset<CMyProviderCommand>*) pThis;  
  
CComQIPtr<IRowsetInfo, &IID_IRowsetInfo> spRowsetProps = pRowset;  
  
DBPROPIDSET set;  
set.AddPropertyID(DBPROP_BOOKMARKS);  

DBPROPSET* pPropSet = NULL;  
ULONG ulPropSet = 0;  

HRESULT hr;  
  
if (spRowsetProps)  
   hr = spRowsetProps->GetProperties(1, &set, &ulPropSet, &pPropSet);  
  

if (pPropSet)  
{  
   CComVariant var = pPropSet->rgProperties[0].vValue;  
   CoTaskMemFree(pPropSet->rgProperties);  
   CoTaskMemFree(pPropSet);  
  
   if (SUCCEEDED(hr) && (var.boolVal == VARIANT_TRUE))  
   {  
      ...  // Use property here  
   }  
}  
```  
  
## <a name="see-also"></a>请参阅  

[使用 OLE DB 提供程序模板](../../data/oledb/working-with-ole-db-provider-templates.md)