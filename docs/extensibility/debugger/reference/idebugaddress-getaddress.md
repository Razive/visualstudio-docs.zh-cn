---
title: IDebugAddress::GetAddress |Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugAddress::GetAddress
helpviewer_keywords:
- IDebugAddress:GetAddress method
ms.assetid: 2590387b-5d36-4116-9a75-737957b8898e
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 8d4a40da82f77f3eb04317fcb936e7a10c5351e8
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/02/2019
ms.locfileid: "53863704"
---
# <a name="idebugaddressgetaddress"></a>IDebugAddress::GetAddress
返回描述对象并将其作用域或容器内的其位置的结构。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetAddress (  
   DEBUG_ADDRESS * pAddress  
);  
```  
  
```csharp  
int GetAddress(  
   DEBUG_ADDRESS[] pAddress  
);  
```  
  
#### <a name="parameters"></a>参数  
 `pAddress`  
 [in、 out]一个[DEBUG_ADDRESS](../../../extensibility/debugger/reference/debug-address.md)通过此方法来填充的结构。  
  
## <a name="return-value"></a>返回值  
 如果成功，则返回 S_OK;否则，返回错误代码。  
  
## <a name="remarks"></a>备注  
 [DEBUG_ADDRESS](../../../extensibility/debugger/reference/debug-address.md)结构传递给此方法，然后使用相应的信息对其进行填充。 如何解释此信息取决于返回的信息和符号处理程序本身的类型。 请参阅[DEBUG_ADDRESS](../../../extensibility/debugger/reference/debug-address.md)的更多详细信息。  
  
## <a name="see-also"></a>请参阅  
 [DEBUG_ADDRESS](../../../extensibility/debugger/reference/debug-address.md)