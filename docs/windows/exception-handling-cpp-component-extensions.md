---
title: 异常处理 （c + + 组件扩展） |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- structured exception handling [C++], managed exceptions
- Exception class, managed applications
- exception handling
- C++ exception handling
- exception handling, types of
- System::Exception class in managed applications
ms.assetid: ccb11fe8-6938-41ac-b477-a183e85865b9
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 2213266d281933c6a6a59775584532acaeb39d6e
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/19/2018
ms.locfileid: "46412311"
---
# <a name="exception-handling--c-component-extensions"></a>异常处理（C++ 组件扩展）

使用应用程序编译`/ZW`编译器选项或`/clr`编译器选项都使用*异常*在程序执行期间处理意外的错误。 以下主题讨论 C++/CX 或 C++/CLI 应用程序中的异常处理。

## <a name="in-this-section"></a>本节内容

[使用托管异常中的基本概念](../dotnet/basic-concepts-in-using-managed-exceptions.md)<br/>
描述引发的异常和使用**尝试**/**捕获**块。

[异常处理在 /CLR 下的行为差异](../dotnet/differences-in-exception-handling-behavior-under-clr.md)<br/>
讨论与 C++ 异常处理的标准行为的区别。

[finally](../dotnet/finally.md)<br/>
讨论如何使用 finally 关键字。

[如何：定义和安装全局异常处理程序](../dotnet/how-to-define-and-install-a-global-exception-handler.md)<br/>
演示如何捕获未经处理的异常。

[如何：在本机代码中捕捉从 MSIL 引发的异常](../dotnet/how-to-catch-exceptions-in-native-code-thrown-from-msil.md)<br/>
讨论如何捕获本机代码中的 CLR 和 C++ 异常。

[如何：定义和安装全局异常处理程序](../dotnet/how-to-define-and-install-a-global-exception-handler.md)<br/>
演示如何捕获所有未经处理的异常。

## <a name="related-sections"></a>相关章节

[异常处理](../cpp/exception-handling-in-visual-cpp.md)<br/>
介绍 C++ 中的异常处理。

## <a name="see-also"></a>请参阅

[适用于运行时平台的组件扩展](../windows/component-extensions-for-runtime-platforms.md)