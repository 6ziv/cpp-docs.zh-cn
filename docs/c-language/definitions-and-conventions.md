---
title: 定义和转换 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
dev_langs:
- C++
helpviewer_keywords:
- nonterminals definition
ms.assetid: f9b3cf5f-6a7c-4a10-9b18-9d4a43efdaeb
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 74a29acfcdc58b068ebabe9bc1c9b033cf801c21
ms.sourcegitcommit: 92dbc4b9bf82fda96da80846c9cfcdba524035af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/05/2018
ms.locfileid: "43760401"
---
# <a name="definitions-and-conventions"></a>定义和转换
终止符是语法定义中的终结点。 不提供其他解决方法。 终止符包括保留字和用户定义的标识符的集。  
  
非终止符是语法中的占位符并在此语法摘要中的其他位置进行定义。 定义可是递归的。  
  
可选组件由带下标的 <sub>opt</sub> 指示。 例如，应用于对象的  
  
> **{** *expression*<sub>opt</sub> **}**
  
指示包含在大括号中的可选表达式。  
  
语法约定对语法的不同组件使用不同的字体特性。 符号和字体如下所示：  
  
|特性|描述|  
|---------------|-----------------|  
|nonterminal|斜体类型指示非终止符。|  
|**const**|粗体类型的终止符是必须按所示方式输入的文本保留字和符号。 此上下文中的字符始终区分大小写。|  
|<sub>opt</sub>|后跟 <sub>opt </sub> 的非终止符始终是可选的。|  
|default typeface|用此字样描述或列出的集中的字符可在 C 语句中用作终止符。|  
  
跟在非终止符之后的冒号 (:) 引入其定义。 替代定义将在单独的行中列出（以单词“one of”开头的情况除外）。  
  
## <a name="see-also"></a>请参阅  
[C 语言语法摘要](../c-language/c-language-syntax-summary.md)