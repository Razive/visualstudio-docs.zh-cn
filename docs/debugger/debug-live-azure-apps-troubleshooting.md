---
title: 快照调试疑难解答 |Microsoft Docs
ms.custom: seodec18
ms.date: 11/07/2017
ms.topic: troubleshooting
helpviewer_keywords:
- debugger
ms.assetid: 511a0697-c68a-4988-9e29-8d0166ca044a
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 3f16206b4c537c141bd90615580934c4481ddf06
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MTE95
ms.contentlocale: zh-CN
ms.lasthandoff: 01/02/2019
ms.locfileid: "53880658"
---
# <a name="troubleshooting-and-known-issues-for-snapshot-debugging-in-visual-studio"></a>快照调试 Visual Studio 中的疑难解答和已知问题

如果在这篇文章中所述的步骤未解决你遇到的问题，请联系snaphelp@microsoft.com。

## <a name="issue-snappoint-does-not-turn-on"></a>问题：吸附点不会启用

如果看到警告图标![吸附点警告图标](../debugger/media/snapshot-troubleshooting-snappoint-warning-icon.png "吸附点警告图标")与你吸附点而不是常规的吸附点图标，然后吸附点未打开。

![吸附点未开启](../debugger/media/snapshot-troubleshooting-dont-turn-on.png "吸附点不会启用")

执行以下步骤：

1. 请确保具有相同版本的用于生成和部署你 app.isua1 的源代码。 请确保要为你的部署加载正确的符号。 若要执行此操作，查看**模块**窗口而快照调试和验证是否为正在调试的模块加载符号文件列显示的.pdb 文件。 快照调试程序将尝试自动下载并为你的部署使用的符号。

## <a name="issue-symbols-do-not-load-when-i-open-a-snapshot"></a>问题：我打开的快照时不加载符号

如果看到以下窗口时，符号未加载。

![未加载符号](../debugger/media/snapshot-troubleshooting-symbols-wont-load.png "未加载符号")

执行以下步骤：

- 单击**更改符号设置...** 此页上的链接。 在中**调试 > 符号**设置，添加一个符号缓存目录。 重新启动快照调试后设置符号路径。

   符号或你的项目中可用的.pdb 文件必须匹配你的应用服务部署。 大多数部署 (通过 Visual Studio、 Azure 管道或 Kudu 中，使用 CI/CD 部署等) 将沿符号文件发布到应用服务。 设置符号缓存目录可使 Visual Studio 以使用这些符号。

   ![符号设置](../debugger/media/snapshot-troubleshooting-symbol-settings.png "符号设置")

- 或者，如果你的组织使用符号服务器，或者将符号放入不同的路径，使用符号设置以加载你的部署正确的符号。

## <a name="issue-i-cannot-see-the-attach-snapshot-debugger-option-in-the-cloud-explorer"></a>问题：看不到云资源管理器中的"附加快照调试器"选项

执行以下步骤：

- 请确保安装了快照调试程序组件。 打开 Visual Studio 安装程序，并检查**快照调试器**组件中的 Azure 工作负荷。
- 请确保您的应用程序支持。 目前，只有 ASP.NET (4.6.1+) 和 ASP.NET Core （2.0 +） 应用部署到 Azure 应用服务支持。

## <a name="issue-i-only-see-throttled-snapshots-in-the-diagnostic-tools"></a>问题：我只看到限制在诊断工具的快照

![Throttled 被阻止的 snappoint](../debugger/media/snapshot-troubleshooting-throttled-snapshots.png "限制吸附点")

执行以下步骤：

- 快照占用很少的内存，但具有认可用量。 如果快照调试程序检测到你的服务器是大量的内存负载下，它将不会快照。 可以通过停止快照调试程序会话，然后重试删除已捕获的快照。

## <a name="known-issues"></a>已知问题

- 当前不支持使用多个 Visual Studio 客户端针对同一个应用服务进行快照调试。
- Roslyn IL 优化不完全支持 ASP.NET Core 项目中。 对于某些 ASP.NET Core 项目，你可能无法再看到某些变量，或在条件语句中使用一些变量。 
- 特殊变量，如 *$FUNCTION*或 *$CALLER*，无法计算条件语句或个记录点，对于 ASP.NET Core 项目中。
- 快照调试不适用于具有的应用服务[本地缓存](/azure/app-service/app-service-local-cache)开启。
- 目前不支持调试 API 应用的快照。

## <a name="site-extension-upgrade"></a>站点扩展升级

快照调试和 Application Insights 依赖于 ICorProfiler，它将加载到站点过程并在升级过程中将导致文件锁定问题。 我们建议使用此过程以确保没有任何停机的情况下为您的生产站点。

- 创建[部署槽](/azure/app-service/web-sites-staged-publishing)让应用服务中并将您的网站部署到槽。
- 从 Visual Studio 中的云资源管理器或从 Azure 门户交换使用的生产槽。
- 停止槽站点。 这将需要几秒钟来关闭从所有实例的站点 w3wp.exe 进程终止。
- 从 Kudu 站点或 Azure 门户升级槽站点扩展 (*应用服务边栏选项卡 > 开发工具 > 扩展 > 更新*)。
- 启动槽站点。 我们建议访问网站来再次预热。
- 使用的生产槽交换。

## <a name="see-also"></a>请参阅

[在 Visual Studio 中进行调试](../debugger/index.md)  
[调试实时 ASP.NET 应用中使用快照调试程序](../debugger/debug-live-azure-applications.md)  
[快照调试常见问题解答](../debugger/debug-live-azure-apps-faq.md)  
