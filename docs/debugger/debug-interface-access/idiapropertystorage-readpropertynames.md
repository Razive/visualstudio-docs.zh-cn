---
title: IDiaPropertyStorage::ReadPropertyNames |Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaPropertyStorage::ReadPropertyNames
ms.assetid: f8bcab77-afca-4a8f-8710-697842f8a518
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 07c9c5d129305d8c3128a081abe8079321043a57
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MTE95
ms.contentlocale: zh-CN
ms.lasthandoff: 01/02/2019
ms.locfileid: "53918948"
---
# <a name="idiapropertystoragereadpropertynames"></a>IDiaPropertyStorage::ReadPropertyNames
检索对应的字符串名称给定属性标识符。  
  
## <a name="syntax"></a>语法  
  
```C++  
HRESULT ReadPropertyNames (  
   ULONG         cpropid,  
   PROPID const* rgpropid,  
   BSTR*         rglpwstrName  
);  
```  
  
#### <a name="parameters"></a>参数  
 `cpropid`  
 [in]中的属性 id 数`rgpropid`。  
  
 `rgpropid`  
 [in]要为其获取名称的属性 id 的数组 (`PROPID`定义为 WTypes.h 中`ULONG`)。  
  
 `rglpwstrName`  
 [in、 out]指定的属性 id 的属性名称的数组。 数组必须是预分配用于保存请求的数目的属性名称，并且必须能够至少容纳`cpropid``BSTR`字符串。  
  
## <a name="return-value"></a>返回值  
 如果成功，则返回`S_OK`; 否则返回错误代码。  
  
## <a name="remarks"></a>备注  
 返回的属性名称，必须释放 (通过调用`SysFreeString`函数) 在不再需要时。  
  
## <a name="see-also"></a>请参阅  
 [IDiaPropertyStorage](../../debugger/debug-interface-access/idiapropertystorage.md)