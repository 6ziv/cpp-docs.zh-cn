---
title: CDBVariant 类 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: reference
f1_keywords:
- CDBVariant
- AFXDB/CDBVariant
- AFXDB/CDBVariant::CDBVariant
- AFXDB/CDBVariant::Clear
- AFXDB/CDBVariant::m_dwType
- AFXDB/CDBVariant::m_boolVal
- AFXDB/CDBVariant::m_chVal
- AFXDB/CDBVariant::m_dblVal
- AFXDB/CDBVariant::m_fltVal
- AFXDB/CDBVariant::m_iVal
- AFXDB/CDBVariant::m_lVal
- AFXDB/CDBVariant::m_pbinary
- AFXDB/CDBVariant::m_pdate
- AFXDB/CDBVariant::m_pstring
- AFXDB/CDBVariant::m_pstringA
- AFXDB/CDBVariant::m_pstringW
dev_langs:
- C++
helpviewer_keywords:
- CDBVariant [MFC], CDBVariant
- CDBVariant [MFC], Clear
- CDBVariant [MFC], m_dwType
- CDBVariant [MFC], m_boolVal
- CDBVariant [MFC], m_chVal
- CDBVariant [MFC], m_dblVal
- CDBVariant [MFC], m_fltVal
- CDBVariant [MFC], m_iVal
- CDBVariant [MFC], m_lVal
- CDBVariant [MFC], m_pbinary
- CDBVariant [MFC], m_pdate
- CDBVariant [MFC], m_pstring
- CDBVariant [MFC], m_pstringA
- CDBVariant [MFC], m_pstringW
ms.assetid: de23609c-c560-4b24-bd6b-9d8903fd5b49
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: e1c3ccdba1de9191079630989facf154ccf62d7f
ms.sourcegitcommit: a41c4d096afca1e9b619bbbce045b77135d32ae2
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/14/2018
ms.locfileid: "42540377"
---
# <a name="cdbvariant-class"></a>CDBVariant 类
表示 MFC ODBC 类的变量数据类型。  
  
## <a name="syntax"></a>语法  
  
```  
class CDBVariant  
```  
  
## <a name="members"></a>成员  
  
### <a name="public-constructors"></a>公共构造函数  
  
|名称|描述|  
|----------|-----------------|  
|[CDBVariant::CDBVariant](#cdbvariant)|构造 `CDBVariant` 对象。|  
  
### <a name="public-methods"></a>公共方法  
  
|名称|描述|  
|----------|-----------------|  
|[CDBVariant::Clear](#clear)|清除`CDBVariant`对象。|  
  
### <a name="public-data-members"></a>公共数据成员  
  
|名称|描述|  
|----------|-----------------|  
|[CDBVariant::m_dwType](#m_dwtype)|包含当前存储的值的数据类型。 键入 `DWORD`。|  
  
### <a name="public-union-members"></a>公共联合成员  
  
|name|描述|  
|----------|-----------------|  
|[CDBVariant::m_boolVal](#m_boolval)|包含类型的值**BOOL**。|  
|[CDBVariant::m_chVal](#m_chval)|包含类型的值**无符号 char**。|  
|[CDBVariant::m_dblVal](#m_dblval)|包含类型的值**double**。|  
|[CDBVariant::m_fltVal](#m_fltval)|包含类型的值**float**。|  
|[CDBVariant::m_iVal](#m_ival)|包含类型的值**短**。|  
|[CDBVariant::m_lVal](#m_lval)|包含类型的值**长**。|  
|[CDBVariant::m_pbinary](#m_pbinary)|包含类型的对象的指针`CLongBinary`。|  
|[CDBVariant::m_pdate](#m_pdate)|包含类型的对象的指针**TIMESTAMP_STRUCT**。|  
|[CDBVariant::m_pstring](#m_pstring)|包含类型的对象的指针`CString`。|  
|[CDBVariant::m_pstringA](#m_pstringa)|存储指向 ASCII [CString](../../atl-mfc-shared/reference/cstringt-class.md)对象。|  
|[CDBVariant::m_pstringW](#m_pstringw)|存储指向宽[CString](../../atl-mfc-shared/reference/cstringt-class.md)对象。|  
  
## <a name="remarks"></a>备注  
 `CDBVariant` 没有基类。  
  
 `CDBVariant` 类似于[COleVariant](../../mfc/reference/colevariant-class.md); 但是，`CDBVariant`不使用 OLE。 `CDBVariant` 可以用来存储值，而无需担心值的数据类型。 `CDBVariant` 跟踪存储在联合中的当前值的数据类型。  
  
 类[CRecordset](../../mfc/reference/crecordset-class.md)利用`CDBVariant`三个成员函数中的对象： `GetFieldValue`， `GetBookmark`，并`SetBookmark`。 例如，`GetFieldValue`允许你动态提取列中的数据。 因为列的数据类型可能不知道在运行时，`GetFieldValue`使用`CDBVariant`对象来存储列的数据。  
  
## <a name="inheritance-hierarchy"></a>继承层次结构  
 `CDBVariant`  
  
## <a name="requirements"></a>要求  
 **标头：** afxdb.h  
  
##  <a name="cdbvariant"></a>  CDBVariant::CDBVariant  
 创建 NULL`CDBVariant`对象。  
  
```  
CDBVariant();
```  
  
### <a name="remarks"></a>备注  
 集[m_dwType](#m_dwtype) DBVT_NULL 到的数据成员。  
  
##  <a name="clear"></a>  CDBVariant::Clear  
 调用此成员函数可清除`CDBVariant`对象。  
  
```  
void Clear();
```  
  
### <a name="remarks"></a>备注  
 如果的值[m_dwType](#m_dwtype)数据成员是 DBVT_DATE、 DBVT_STRING，还是 DBVT_BINARY，`Clear`释放与联合的指针成员相关联的内存。 `Clear` 设置`m_dwType`DBVT_NULL 到。  
  
 `CDBVariant`析构函数调用`Clear`。  
  
##  <a name="m_boolval"></a>  CDBVariant::m_boolVal  
 存储类型 BOOL 的值。  
  
### <a name="remarks"></a>备注  
 `m_boolVal`属于联合数据成员。 在访问之前`m_boolVal`，首先检查的值[CDBVariant::m_dwType](#m_dwtype)。 如果`m_dwType`设置为 DBVT_BOOL，则`m_boolVal`将包含一个有效的值; 否则为访问`m_boolVal`将生成不可靠的结果。  
  
##  <a name="m_chval"></a>  CDBVariant::m_chVal  
 存储类型的值**无符号 char**。  
  
### <a name="remarks"></a>备注  
 `m_chVal`属于联合数据成员。 在访问之前`m_chVal`，首先检查的值[CDBVariant::m_dwType](#m_dwtype)。 如果`m_dwType`设置为 DBVT_UCHAR，则`m_chVal`包含有效的值; 否则为访问`m_chVal`将生成不可靠的结果。  
  
##  <a name="m_dblval"></a>  CDBVariant::m_dblVal  
 存储类型的值**double**。  
  
### <a name="remarks"></a>备注  
 `m_dblVal`属于联合数据成员。 在访问之前`m_dblVal`，首先检查的值[CDBVariant::m_dwType](#m_dwtype)。 如果`m_dwType`设置为 DBVT_DOUBLE，则`m_dblVal`包含有效的值; 否则为访问`m_dblVal`将生成不可靠的结果。  
  
##  <a name="m_dwtype"></a>  CDBVariant::m_dwType  
 此数据成员包含在当前存储的值的数据类型`CDBVariant`对象的联合数据成员。  
  
### <a name="remarks"></a>备注  
 在访问前此并集，必须检查的值`m_dwType`以便确定哪些联合数据成员才能访问。 下表列出了可能的值为`m_dwType`和相应的联合数据成员。  
  
|m_dwType|联合数据成员|  
|---------------|-----------------------|  
|DBVT_NULL|任何联合成员不是有效的访问权限。|  
|DBVT_BOOL|[m_boolVal](#m_boolval)|  
|DBVT_UCHAR|[m_chVal](#m_chval)|  
|DBVT_SHORT|[m_iVal](#m_ival)|  
|DBVT_LONG|[m_lVal](#m_lval)|  
|DBVT_SINGLE|[m_fltVal](#m_fltval)|  
|DBVT_DOUBLE|[m_dblVal](#m_dblval)|  
|DBVT_DATE|[m_pdate](#m_pdate)|  
|DBVT_STRING|[m_pstring](#m_pstring)|  
|DBVT_BINARY|[m_pbinary](#m_pbinary)|  
|DBVT_ASTRING|[m_pstringA](#m_pstringa)|  
|DBVT_WSTRING|[m_pstringW](#m_pstringw)|  
  
##  <a name="m_fltval"></a>  CDBVariant::m_fltVal  
 存储类型的值**float**。  
  
### <a name="remarks"></a>备注  
 `m_fltVal`属于联合数据成员。 在访问之前`m_fltVal`，首先检查的值[CDBVariant::m_dwType](#m_dwtype)。 如果`m_dwType`设置为 DBVT_SINGLE，则`m_fltVal`包含有效的值; 否则为访问`m_fltVal`将生成不可靠的结果。  
  
##  <a name="m_ival"></a>  CDBVariant::m_iVal  
 存储类型的值**短**。  
  
### <a name="remarks"></a>备注  
 `m_iVal`属于联合数据成员。 在访问之前`m_iVal`，首先检查的值[CDBVariant::m_dwType](#m_dwtype)。 如果`m_dwType`设置为 DBVT_SHORT，则`m_iVal`包含有效的值; 否则为访问`m_iVal`将生成不可靠的结果。  
  
##  <a name="m_lval"></a>  CDBVariant::m_lVal  
 存储类型的值**长**。  
  
### <a name="remarks"></a>备注  
 `m_lVal`属于联合数据成员。 在访问之前`m_lVal`，首先检查的值[CDBVariant::m_dwType](#m_dwtype)。 如果`m_dwType`设置为 DBVT_LONG，则`m_lVal`包含有效的值; 否则为访问`m_lVal`将生成不可靠的结果。  
  
##  <a name="m_pbinary"></a>  CDBVariant::m_pbinary  
 存储指向类型的对象的指针[CLongBinary](../../mfc/reference/clongbinary-class.md)。  
  
### <a name="remarks"></a>备注  
 `m_pbinary`属于联合数据成员。 在访问之前`m_pbinary`，首先检查的值[CDBVariant::m_dwType](#m_dwtype)。 如果`m_dwType`设置为 DBVT_BINARY，则`m_pbinary`包含有效的指针; 否则为访问`m_pbinary`将生成不可靠的结果。  
  
##  <a name="m_pdate"></a>  CDBVariant::m_pdate  
 存储指向类型 TIMESTAMP_STRUCT 的对象的指针。  
  
### <a name="remarks"></a>备注  
 `m_pdate`属于联合数据成员。 在访问之前`m_pdate`，首先检查的值[CDBVariant::m_dwType](#m_dwtype)。 如果`m_dwType`设置为 DBVT_DATE，则`m_pdate`包含有效的指针; 否则为访问`m_pdate`将生成不可靠的结果。  
  
 有关 TIMESTAMP_STRUCT 数据类型的详细信息，请参阅主题[C 数据类型](/previous-versions/windows/desktop/ms714556\(v=vs.85\))中的附录 D *ODBC 程序员参考*Windows SDK 中。  
  
##  <a name="m_pstring"></a>  CDBVariant::m_pstring  
 存储指向类型的对象的指针[CString](../../atl-mfc-shared/reference/cstringt-class.md)。  
  
### <a name="remarks"></a>备注  
 `m_pstring`属于联合数据成员。 在访问之前`m_pstring`，首先检查的值[CDBVariant::m_dwType](#m_dwtype)。 如果`m_dwType`设置为 DBVT_STRING，则`m_pstring`包含有效的指针; 否则为访问`m_pstring`将生成不可靠的结果。  
  
##  <a name="m_pstringa"></a>  CDBVariant::m_pstringA  
 存储指向 ASCII [CString](../../atl-mfc-shared/reference/cstringt-class.md)对象。  
  
### <a name="remarks"></a>备注  
 `m_pstringA`属于联合数据成员。 在访问之前`m_pstringA`，首先检查的值[CDBVariant::m_dwType](#m_dwtype)。 如果`m_dwType`设置为 DBVT_ASTRING，则`m_pstringA`包含有效的指针; 否则为访问`m_pstringA`将生成不可靠的结果。  
  
##  <a name="m_pstringw"></a>  CDBVariant::m_pstringW  
 存储指向宽[CString](../../atl-mfc-shared/reference/cstringt-class.md)对象。  
  
### <a name="remarks"></a>备注  
 `m_pstringW`属于联合数据成员。 在访问之前`m_pstringW`，首先检查的值[CDBVariant::m_dwType](#m_dwtype)。 如果`m_dwType`设置为 DBVT_WSTRING，则`m_pstringW`包含有效的指针; 否则为访问`m_pstringW`将生成不可靠的结果。  
  
## <a name="see-also"></a>请参阅  
 [层次结构图表](../../mfc/hierarchy-chart.md)   
 [CRecordset 类](../../mfc/reference/crecordset-class.md)
