---
title: 编译器警告 （等级 1） C4251 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4251
dev_langs:
- C++
helpviewer_keywords:
- C4251
ms.assetid: a9992038-f0c2-4fc4-a9be-4509442cbc1e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ad47d769dbfd09cc741be18598355dc34486bd54
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2018
ms.locfileid: "46045687"
---
# <a name="compiler-warning-level-1-c4251"></a>编译器警告（等级 1）C4251

identifier： 类 type 需要有 dll 接口的类 type2 的客户端使用

若要导出具有的类时，数据损坏的可能性降至最低[__declspec （dllexport)](../../cpp/dllexport-dllimport.md)，，请确保：

- 所有静态数据是通过从 DLL 导出的函数的访问。

- 您的类没有内联的方法可以修改静态数据。

- 您的类没有内联的方法使用的 CRT 函数或其他库函数使用静态数据 (请参阅[潜在错误对象跨 DLL 边界传递 CRT](../../c-runtime-library/potential-errors-passing-crt-objects-across-dll-boundaries.md)有关详细信息)。

- 您的类没有方法 (而不考虑内联) 可以使用类型其中 EXE 和 DLL 中的实例化具有静态数据的差异。

您可以避免通过定义一个 DLL，它定义了具有虚函数的类和函数，可以调用来实例化并删除对象类型的导出类。  然后，可以只需调用虚函数的类型。

导出模板的详细信息，请参阅[ http://support.microsoft.com/default.aspx?scid=KB;EN-US; 168958](http://support.microsoft.com/default.aspx?scid=KB;EN-US;168958)。

如果从 c + + 标准库，编译调试版本中的类型派生，则可以忽略 C4251 (**/MTd**)，其中编译器错误消息是指 _Container_base。

```
// C4251.cpp
// compile with: /EHsc /MTd /W2 /c
#include <vector>
using namespace std;
class Node;
class __declspec(dllimport) VecWrapper : vector<Node *> {};   // C4251
```