---
title: '#错误指令 （C/c + +） |Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- '#error'
dev_langs:
- C++
helpviewer_keywords:
- '#error directive'
- preprocessor, directives
- error directive (#error directive)
ms.assetid: d550a802-ff19-4347-9597-688935d23b2b
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d2da939fe52e41e122ecd4926e34fb9c4be735ae
ms.sourcegitcommit: d4c803bd3a684d7951bf88dcecf1f14af43ae411
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/10/2018
ms.locfileid: "42540946"
---
# <a name="error-directive-cc"></a>#error 指令 (C/C++)
**#Error**指令在编译时发出用户指定的错误消息，然后终止编译。  
  
## <a name="syntax"></a>语法  
  
```  
#errortoken-string  
```  
  
## <a name="remarks"></a>备注  
 
此指令发出的错误消息包括*令牌字符串*参数。 *令牌字符串*参数不受宏扩展。 此指令通知程序不一致的开发人员或违反约束在预处理过程会十分有用。 下面的示例演示如何处理在预处理期间出错：  
  
```  
#if !defined(__cplusplus)  
#error C++ compiler required.  
#endif  
```  
  
## <a name="see-also"></a>请参阅  
 
[预处理器指令](../preprocessor/preprocessor-directives.md)