---
title: 客户体验改善计划
description: 了解如何在 Visual Studio 中管理隐私设置。
ms.date: 05/21/2018
ms.prod: visual-studio-dev15
ms.topic: conceptual
author: PoulChapman
ms.author: tglee
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 71205231e3734fd5df876501f3880afa8b0779c5
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/02/2019
ms.locfileid: "53822766"
---
# <a name="visual-studio-customer-experience-improvement-program"></a>Visual Studio 客户体验改善计划

Visual Studio 客户体验改善计划 (VSCEIP) 旨在随着时间推移帮助 Microsoft 改进 Visual Studio。 此程序[收集有关错误的信息](../ide/diagnostic-data-collection.md)、计算机硬件以及 Visual Studio 的使用方式，而不中断用户在计算机中的任务。 收集的信息帮助 Microsoft 确定要改善的功能。 本文档介绍如何选择加入或退出 VSCEIP。

[!INCLUDE [gdpr-hybrid-note](../misc/includes/gdpr-hybrid-note.md)]

## <a name="opt-in-or-out"></a>选择加入或退出

VSCEIP 默认开启。 可以按照以下步骤将其关闭或者再次打开：

1. 启动 Visual Studio。

1. 从“帮助”菜单，指向“发送反馈”，然后选择“设置”。

   “Visual Studio 体验改善计划”对话框随即打开。

1. 若要选择退出，请选择“否，我不想参加”，然后选择“确定”。
   若要选择加入，请选择“是，我愿意参加”，然后选择“确定”。

   ![“Visual Studio 体验改善计划”对话框](media/experience-improvement-program.png)

### <a name="registry-settings"></a>注册表设置

如果安装 [Visual Studio 生成工具](https://visualstudio.microsoft.com/downloads/#build-tools-for-visual-studio-2017)，必须更新注册表来配置 VSCEIP。 企业客户可以设置基于注册表的策略，利用这种方式构造选择加入或不加入 VSCEIP 的组策略。

相关注册表项和设置如下所示：

在 64 位操作系统上，Key = HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\VSCommon\15.0\SQM 在 32 位操作系统上，Key = HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\VSCommon\15.0\SQM 启用组策略时，Key = HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\VisualStudio\SQM

Entry = OptIn

Value = (DWORD)
- “0”为选择退出（关闭 VSCEIP）
- “1”为选择加入（开启 VSCEIP）

> [!CAUTION]
> 错误地编辑注册表可能会严重损坏您的系统。 在对注册表进行更改之前，应备份计算机上任何有价值的数据。 如果在应用手动更改之后遇到问题，也可以使用“最近一次的正确配置”启动选项。

有关 VSCEIP 收集、处理或传输的信息的详情，请参阅 [Microsoft 隐私声明](https://privacy.microsoft.com/privacystatement)。

## <a name="see-also"></a>请参阅

* [Visual Studio 收集的诊断信息](diagnostic-data-collection.md)
* [与我们交流](../ide/talk-to-us.md)
* [如何报告 Visual Studio 的问题](../ide/how-to-report-a-problem-with-visual-studio-2017.md)
* [Visual Studio 开发者社区](https://developercommunity.visualstudio.com/)
* [Microsoft 隐私声明](https://privacy.microsoft.com/privacystatement)
