---
title: IDebugDocumentContext2::GetSourceRange |Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugDocumentContext2::GetSourceRange
helpviewer_keywords:
- IDebugDocumentContext2::GetSourceRange
ms.assetid: 5903c75e-5390-4d13-9314-1ee276255313
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: fe2ad435b4b70f2314822414c0cc0eb429c2478e
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/02/2019
ms.locfileid: "53841550"
---
# <a name="idebugdocumentcontext2getsourcerange"></a>IDebugDocumentContext2::GetSourceRange
获取此文档上下文的源的代码范围。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetSourceRange(   
   TEXT_POSITION* pBegPosition,  
   TEXT_POSITION* pEndPosition  
);  
```  
  
```csharp  
int GetSourceRange(   
   TEXT_POSITION[] pBegPosition,  
   TEXT_POSITION[] pEndPosition  
);  
```  
  
#### <a name="parameters"></a>参数  
 `pBegPosition`  
 [in、 out]一个[TEXT_POSITION](../../../extensibility/debugger/reference/text-position.md)填充的起始位置的结构。 如果不需要此信息，请将此参数设置为 null 值。  
  
 `pEndPosition`  
 [in、 out]一个[TEXT_POSITION](../../../extensibility/debugger/reference/text-position.md)填充的结束位置的结构。 如果不需要此信息，请将此参数设置为 null 值。  
  
## <a name="return-value"></a>返回值  
 如果成功，则返回`S_OK`; 否则为返回错误代码。  
  
## <a name="remarks"></a>备注  
 源范围是源代码，从当前的语句后，前面代码的语句之后的整个范围。 源范围通常用于混合源语句，其中包括注释，使用反汇编窗口中的代码。  
  
 若要获取的只是包含在此文档上下文中的代码语句的范围，请调用[GetStatementRange](../../../extensibility/debugger/reference/idebugdocumentcontext2-getstatementrange.md)方法。  
  
## <a name="see-also"></a>请参阅  
 [IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md)   
 [GetStatementRange](../../../extensibility/debugger/reference/idebugdocumentcontext2-getstatementrange.md)   
 [TEXT_POSITION](../../../extensibility/debugger/reference/text-position.md)