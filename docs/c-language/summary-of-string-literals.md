---
title: 字符串文本摘要 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
dev_langs:
- C++
ms.assetid: d2693900-f4e2-4820-b7de-085d51827aee
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: a94d575ee36f38b56f64fb6298eb6f6f6e43567e
ms.sourcegitcommit: 92dbc4b9bf82fda96da80846c9cfcdba524035af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/05/2018
ms.locfileid: "43762738"
---
# <a name="summary-of-string-literals"></a>字符串文本的摘要

string-literal：<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**'** *s-char-sequence*<sub>opt</sub> **'**<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**L'** *s-char-sequence*sub>opt</sub> **'**  
  
s-char-sequence：<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*s-char*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*s-char-sequence* *s-char*  
  
s-char：<br/>
&nbsp;&nbsp;&nbsp;&nbsp;除双引号 (")、反斜杠 (\\) 或换行符 escape-sequence 之外的源字符集的任何成员  

## <a name="see-also"></a>请参阅

[词法语法](../c-language/lexical-grammar.md)