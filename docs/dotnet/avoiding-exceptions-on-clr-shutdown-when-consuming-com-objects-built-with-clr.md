---
title: 避免使用-clr 生成 COM 对象由引发的异常 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- interop [C++], CLR shutdown exceptions
- /clr compiler option [C++], CLR shutdown exceptions
- mixed assemblies [C++], CLR shutdown exceptions
- /clr compiler option [C++], COM objects
- interoperability [C++], CLR shutdown exceptions
- CLR shutdown exceptions [C++]
ms.assetid: 41249d83-4b51-4e46-866f-27f475f2498c
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 687585d0b25c64f5575646de3cd4823e0a89988e
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/19/2018
ms.locfileid: "46408959"
---
# <a name="avoiding-exceptions-on-clr-shutdown-when-consuming-com-objects-built-with-clr"></a>使用以 /clr 生成的 COM 对象时避免 CLR 关闭异常

公共语言运行时 (CLR) 进入后关闭模式，本机函数会限制对 CLR 服务的访问。 编译的 COM 对象时尝试对其调用 Release **/clr**CLR 转换为本机代码，然后转换回为 iunknown:: Release 呼叫 （这在托管代码中定义） 提供服务的托管代码。 CLR 会阻止返回到托管代码调用，因为它是处于关闭状态。

若要解决此问题，请确保从 Release 方法调用的析构函数只能包含本机代码。

## <a name="see-also"></a>请参阅

[混合（本机和托管）程序集](../dotnet/mixed-native-and-managed-assemblies.md)