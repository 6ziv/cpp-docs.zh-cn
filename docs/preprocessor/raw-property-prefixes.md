---
title: raw_property_prefixes |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- raw_property_prefixes
dev_langs:
- C++
helpviewer_keywords:
- raw_property_prefixes attribute
ms.assetid: 03a0f48c-c460-4175-a762-9f7f8d84b12f
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 3ae69e26077692188b8e013e949592df26d7701a
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/19/2018
ms.locfileid: "46420395"
---
# <a name="rawpropertyprefixes"></a>raw_property_prefixes
**C + + 专用**  
  
指定用于三个属性方法的备用前缀。  
  
## <a name="syntax"></a>语法  
  
```  
raw_property_prefixes("GetPrefix","PutPrefix","PutRefPrefix")  
```  
  
### <a name="parameters"></a>参数  
*GetPrefix*  
前缀用于`propget`方法。  
  
*PutPrefix*  
前缀用于`propput`方法。  
  
*PutRefPrefix*  
前缀用于`propputref`方法。  
  
## <a name="remarks"></a>备注  
 
默认情况下，低级别`propget`， `propput`，并`propputref`具有前缀的命名的成员函数公开方法**get_**， **put_**，和**putref_** 分别。 这些前缀与在 MIDL 生成的标头文件中使用的名称兼容。  
  
**结束 c + + 专用**  
  
## <a name="see-also"></a>请参阅  
 
[#import 属性](../preprocessor/hash-import-attributes-cpp.md)<br/>
[#import 指令](../preprocessor/hash-import-directive-cpp.md)