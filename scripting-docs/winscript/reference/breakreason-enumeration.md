---
title: BREAKREASON 枚举 |Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- BREAKREASON
apilocation:
- scrobj.dll
helpviewer_keywords:
- BREAKREASON enumeration
ms.assetid: bde07ede-2f9b-4fa2-affc-f9405683f5f7
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d5c0dc03d8d24014e28ecf9510fa3d5faa21dba2
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/08/2019
ms.locfileid: "54096793"
---
# <a name="breakreason-enumeration"></a>BREAKREASON 枚举
指示造成中断的原因。  
  
## <a name="syntax"></a>语法  
  
```cpp
typedef enum tagBREAKREASON {  
   BREAKREASON_STEP,  
   BREAKREASON_BREAKPOINT,  
   BREAKREASON_DEBUGGER_BLOCK,  
   BREAKREASON_HOST_INITIATED,  
   BREAKREASON_LANGUAGE_INITIATED,  
   BREAKREASON_DEBUGGER_HALT,  
   BREAKREASON_ERROR,  
   BREAKREASON_JIT  
} BREAKREASON;  
```  
  
## <a name="members"></a>成员  
  
|成员|描述|  
|------------|-----------------|  
|BREAKREASON_STEP|语言引擎是在单步执行模式下。|  
|BREAKREASON_BREAKPOINT|语言引擎遇到显式断点。|  
|BREAKREASON_DEBUGGER_BLOCK|语言引擎遇到另一个线程上的调试程序块。|  
|BREAKREASON_HOST_INITIATED|主机请求一个分行符。|  
|BREAKREASON_LANGUAGE_INITIATED|语言引擎请求一个分行符。|  
|BREAKREASON_DEBUGGER_HALT|调试器 IDE 请求一个分行符。|  
|会发生 BREAKREASON_ERROR|执行错误造成中断的原因。|  
|BREAKREASON_JIT|由 JIT 调试启动引起。|  
  
## <a name="see-also"></a>请参阅  
 [活动脚本调试器常量、枚举和结构](../../winscript/reference/active-script-debugger-constants-enumerations-and-structures.md)