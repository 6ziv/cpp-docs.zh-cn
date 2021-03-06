---
title: -ALLOWISOLATION （清单查找） |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- /ALLOWISOLATION
- VC.Project.VCLinkerTool.AllowIsolation
dev_langs:
- C++
helpviewer_keywords:
- -ALLOWISOLATION linker option
- /ALLOWISOLATION linker option
ms.assetid: 6d41851e-b3c1-4bdf-beaa-031773089d6f
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: c9197e67e46932f08a266258c41dab7922af2900
ms.sourcegitcommit: f0c90000125a9497bf61e41624de189a043703c0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/10/2018
ms.locfileid: "44318975"
---
# <a name="allowisolation-manifest-lookup"></a>/ALLOWISOLATION（清单查找）

指定清单查找的行为。

## <a name="syntax"></a>语法

```
/ALLOWISOLATION[:NO]
```

## <a name="remarks"></a>备注

**/ALLOWISOLATION:NO**指示像没有清单，将加载 Dll，并使链接器设置`IMAGE_DLLCHARACTERISTICS_NO_ISOLATION`可选标头的位`DllCharacteristics`字段。

**/ALLOWISOLATION**会导致操作系统进行清单查找和加载。

**/ALLOWISOLATION**是默认值。

当可执行文件禁用隔离时，Windows 加载程序不会尝试查找新创建的进程的应用程序清单。 新进程将具有默认激活上下文，即使在可执行文件或名称的可执行文件所在的同一目录中放置一个清单<em>可执行文件名称</em>**.exe.manifest 的清单**。

有关详细信息，请参阅[清单文件参考](/windows/desktop/SbsCs/manifest-files-reference)。

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>在 Visual Studio 开发环境中设置此链接器选项

1. 打开项目的“属性页”  对话框。 有关详细信息，请参阅[使用项目属性](../../ide/working-with-project-properties.md)。

1. 选择**配置属性** > **链接器** > **清单文件**属性页。

1. 修改**允许隔离**属性。

## <a name="see-also"></a>请参阅

[设置链接器选项](../../build/reference/setting-linker-options.md)<br/>
[链接器选项](../../build/reference/linker-options.md)
