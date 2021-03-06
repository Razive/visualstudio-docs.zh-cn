---
title: 快速操作、灯泡和螺丝刀
ms.date: 03/28/2018
ms.prod: visual-studio-dev15
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: douge
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: cad90eeea8f4fccb3a331fc3c41d072e03dca80c
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/02/2019
ms.locfileid: "53904664"
---
# <a name="quick-actions"></a>快速操作

通过快速操作，只凭单个操作便可轻松重构、生成或修改代码。 快速操作可用于 C#、[C++](/cpp/ide/writing-and-refactoring-code-cpp) 和 Visual Basic 代码文件。 某些操作特定于一种语言，而其他操作适用于所有语言。

可使用“快速操作”功能：

- 通过代码修复[代码分析器](../code-quality/roslyn-analyzers-overview.md)规则冲突
- [阻止](../code-quality/use-roslyn-analyzers.md)代码分析器规则冲突
- 应用重构（例如，[内联临时变量](../ide/reference/inline-temporary-variable.md)）
- 生成代码（例如，[引入局部变量](../ide/reference/introduce-local-variable.md)）

> [!NOTE]
> 本主题适用于 Windows 上的 Visual Studio。 对于 Visual Studio for Mac，请参阅[重构 (Visual Studio for Mac)](/visualstudio/mac/refactoring)。

可使用灯泡![灯泡图标](media/light-bulb-icon.png)或螺丝刀![螺丝刀图标](media/screwdriver-icon.png)图标，或按“Ctrl”应用快速操作。+ 当光标位于可操作的代码行上时， 如果出现指示错误的红色波形曲线，且 Visual Studio 有针对该错误的可用修复方法，会显示一个错误灯泡![错误灯泡图标](media/error-light-bulb-icon.png)。

第三方可针对任何语言提供自定义诊断和建议，例如随附 SDK 提供，同时根据这些规则，Visual Studio 电灯泡可能亮起。

## <a name="icons"></a>图标

当存在可用的快速操作时，会出现一个图标，指示可用的修复方法或重构的类型。 螺丝刀![螺丝刀图标](media/screwdriver-icon.png)图标仅指示存在可用于更改代码的操作，但不一定要使用它们。 黄色灯泡![灯泡图标](media/light-bulb-icon.png)图标指示存在应执行的、用于改进代码的可用操作。 错误灯泡![错误灯泡图标](media/error-light-bulb-icon.png)图标指示存在可用于修复代码中的错误的操作。

## <a name="to-see-a-light-bulb-or-screwdriver"></a>查看灯泡或螺丝刀

- 如果有可用的修复方法，将鼠标悬停在存在错误的位置时，会同时显示灯泡。

   ![带鼠标悬停的灯泡](../ide/media/vs2015_lightbulb_hover.png)

- 将脱字号移动到可使用快速操作的代码行时，编辑器左边距中会显示灯泡和螺丝刀。

- 按“Ctrl”+**。** 可在行的任意位置查看可用快速操作和重构的列表。

## <a name="to-see-potential-fixes"></a>查看潜在修复

选择灯泡旁边的下箭头或“显示潜在修复”链接，以显示可用快速操作的列表。

![灯泡已展开](../ide/media/vs2015_lightbulb_hover_expanded.png)

## <a name="see-also"></a>请参阅

- [Visual Studio 中的代码生成](../ide/code-generation-in-visual-studio.md)
- [常见快速操作](../ide/common-quick-actions.md)
- [代码样式和快速操作](../ide/code-styles-and-quick-actions.md)
- [编写和重构代码 (C++)](/cpp/ide/writing-and-refactoring-code-cpp)
- [重构 (Visual Studio for Mac)](/visualstudio/mac/refactoring)