---
title: 提取数据 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-data
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- data [C++], fetching
- rowsets [C++], fetching
- fetching
- OLE DB consumer templates [C++], fetching data
ms.assetid: b07f747f-9855-4f27-a03d-b1d5b10fa284
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 05cfcb59100f1778b0266636fb3930fd9489e917
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2018
ms.locfileid: "46067072"
---
# <a name="fetching-data"></a>提取数据

打开数据源、 会话和行集对象后，可以提取数据。 具体取决于正在使用的访问器的类型，可能需要将列绑定。  
  
### <a name="to-fetch-data"></a>若要提取的数据  
  
1. 打开使用相应的行集**打开**命令。  
  
1. 如果使用的`CManualAccessor`，绑定的输出列，如果尚未这样做。 若要绑定的列，调用`GetColumnInfo`，，然后使用绑定创建取值函数，如下面的示例中所示：  
  
    ```cpp  
    // From the DBViewer Sample CDBTreeView::OnQueryEdit  
    // Get the column information  
    ULONG ulColumns       = 0;  
    DBCOLUMNINFO* pColumnInfo  = NULL;  
    LPOLESTR pStrings      = NULL;  
    if (rs.GetColumnInfo(&ulColumns, &pColumnInfo, &pStrings) != S_OK)  
        ThrowMyOLEDBException(rs.m_pRowset, IID_IColumnsInfo);  
    struct MYBIND* pBind = new MYBIND[ulColumns];  
    rs.CreateAccessor(ulColumns, &pBind[0], sizeof(MYBIND)*ulColumns);  
    for (ULONG l=0; l<ulColumns; l++)  
    rs.AddBindEntry(l+1, DBTYPE_STR, sizeof(TCHAR)*40, &pBind[l].szValue, NULL, &pBind[l].dwStatus);  
    rs.Bind();  
    ```  
  
1. 编写`while`循环，以检索数据。 在循环中，调用`MoveNext`前进游标和测试，则为 S_OK，针对返回的值，如下面的示例中所示：  
  
    ```cpp  
    while (rs.MoveNext() == S_OK)  
    {  
        // Add code to fetch data here  
        // If you are not using an auto accessor, call rs.GetData()  
    }  
    ```  
  
1. 在`while`循环中，您可以根据你访问器的类型获取数据。  
  
    -   如果您使用[CAccessor](../../data/oledb/caccessor-class.md)类，您应该具有一个包含数据成员的用户记录。 可以访问使用这些数据成员，您的数据，如下面的示例中所示：  
  
        ```cpp  
        while (rs.MoveNext() == S_OK)  
        {  
            // Use the data members directly. In this case, m_nFooID  
            // is declared in a user record that derives from  
            // CAccessor  
            wsprintf_s("%d", rs.m_nFooID);   
        }  
        ```  
  
    -   如果您使用`CDynamicAccessor`或`CDynamicParameterAccessor`类，就可以通过使用访问函数获取数据`GetValue`和`GetColumn`，如以下示例所示。 如果你想要确定的数据类型使用，请使用`GetType`。  
  
        ```cpp  
        while (rs.MoveNext() == S_OK)  
        {  
            // Use the dynamic accessor functions to retrieve your data.  
  
            ULONG ulColumns = rs.GetColumnCount();  
            for (ULONG i=0; i<ulColumns; i++)  
            {  
                rs.GetValue(i);  
            }  
        }  
        ```  
  
    -   如果使用`CManualAccessor`，必须指定您自己的数据成员，将其绑定自己，并直接访问它们，如下面的示例中所示：  
  
        ```cpp  
        while (rs.MoveNext() == S_OK)  
        {  
            // Use the data members you specified in the calls to  
            // AddBindEntry.  
  
            wsprintf_s("%s", szFoo);  
        }  
        ```  
  
## <a name="see-also"></a>请参阅  

[使用 OLE DB 使用者模板](../../data/oledb/working-with-ole-db-consumer-templates.md)