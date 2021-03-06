---
title: ATL 属性页向导 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-atl
ms.topic: reference
f1_keywords:
- vc.codewiz.class.atl.ppg.overview
dev_langs:
- C++
helpviewer_keywords:
- ATL projects, adding property pages
- ATL Property Page Wizard
ms.assetid: 6113e325-facd-4f68-b491-144d75209922
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: b5a150a81ea26e34e05cbfb9199c734a1ccad9b7
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2018
ms.locfileid: "46094190"
---
# <a name="atl-property-page-wizard"></a>ATL 属性页向导

此向导[将属性页添加到 ATL 项目](../../atl/reference/adding-an-atl-property-page.md)或向 MFC 项目与 ATL 支持。 ATL 属性页来设置属性提供的用户界面 （或调用的方法） 的一个或多个 COM 对象。

## <a name="remarks"></a>备注

从 Visual Studio 2008 开始，此向导生成的注册脚本将注册其 COM 组件**HKEY_CURRENT_USER**而不是**HKEY_LOCAL_MACHINE**。 若要修改此行为，请设置**的所有用户注册组件**ATL 向导的选项。

## <a name="names"></a>名称

指定的对象、 接口和类添加到你的项目的名称。 除**短名称**，可以单独编辑所有其他框。 如果您更改的文本**短名称**，更改都反映在此页中的所有其他框的名称。 如果您更改**组件类**名称在 COM 部分中，更改将反映在**类型**并**ProgID**框。 此命名行为设计以使所有名称轻松地识别为您开发属性页。

> [!NOTE]
>  **组件类**是仅非特性化项目可编辑的。 如果你的项目属性化，则不能编辑**组件类**。

### <a name="c"></a>C++

提供创建要实现对象的 c + + 类的信息。

|||
|-|-|
|术语|定义|
|**短名称**|设置对象的缩写的名称。 你提供的名称确定类和**组件类**命名的文件 (**.cpp**并 **.h**) 的名称，**类型**名称和**ProgID**，除非您单独更改这些字段。|
|**.h 文件**|为新项目的类的头文件设置名称。 默认情况下，此名称基于您在中提供的名称**短名称**。 单击省略号按钮以将该文件名保存至所选择的位置，或追加到某个现有文件的类声明中。 如果选择一个现有文件，该向导将不将其保存到所选位置直到您单击**完成**向导中。<br /><br /> 向导不会覆盖文件。 如果选择现有文件的名称，当你单击“完成”时，向导会询问你是否要将该类声明追加至文件的内容中。 单击“是”，则追加该文件；单击“否”，则返回至向导并指定另一个文件名。|
|**类**|设置实现对象的类的名称。 此名称基于您在中提供的名称**短名称**后, 跟 C，这是典型的类名前缀。|
|**.cpp 文件**|为新项目的类的实现文件设置名称。 默认情况下，此名称基于您在中提供的名称**短名称**。 单击省略号按钮以将文件名保存到所选位置。 向导在你单击“完成”之前不会将该文件保存到所选位置。<br /><br /> 向导不会覆盖文件。 如果选择现有文件的名称，当你单击“完成”时，向导会询问你是否要将该类实现追加至文件的内容中。 单击“是”，则追加该文件；单击“否”，则返回至向导并指定另一个文件名。|
|**特性化**|指示对象是否使用属性。 如果您向特性化 ATL 项目中添加对象，则选择此选项不能更改，也就是说，您可以添加仅归属于创建具有属性支持的项目对象。<br /><br /> 可以仅向使用特性的 ATL 项目添加的特性化的对象。 如果选择此选项为不具有支持的属性的 ATL 项目时，向导会提示您指定是否想要添加到项目的属性的支持。<br /><br /> 默认情况下，设置此选项后添加的任何对象都被指定为特性化 （选中复选框）。 您可以清除此框，可以添加不使用属性的对象。<br /><br /> 请参阅[应用程序设置，ATL 项目向导](../../atl/reference/application-settings-atl-project-wizard.md)并[属性的基本结构](../../windows/basic-mechanics-of-attributes.md)有关详细信息。|

### <a name="com"></a>COM

为对象提供的 COM 功能有关的信息。

- **组件类**

   设置包含一系列对象支持的接口的组件类的名称。

   > [!NOTE]
   > 如果创建你的项目使用特性，或在此向导页上的属性页，使用属性，则不能更改此选项，因为 ATL 不包括`coclass`属性。

- **Type**

   设置会在注册表中的对象说明

- **ProgID**

   设置容器可以使用而不是对象的 CLSID 的名称。

## <a name="see-also"></a>请参阅

[选项，ATL 属性页向导](../../atl/reference/options-atl-property-page-wizard.md)<br/>
[字符串，ATL 属性页向导](../../atl/reference/strings-atl-property-page-wizard.md)<br/>
[示例：实现属性页](../../atl/example-implementing-a-property-page.md)

