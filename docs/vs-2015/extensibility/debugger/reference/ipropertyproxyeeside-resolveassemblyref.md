---
title: IPropertyProxyEESide::ResolveAssemblyRef |Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IPropertyProxyEESide::ResolveAssemblyRef
helpviewer_keywords:
- IPropertyProxyEESide::ResolveAssemblyRef
ms.assetid: 662ca0a6-dad0-4c00-a718-bb3bbc5bd9da
caps.latest.revision: 13
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: ccf17bf9c0a700312d04325f571d6979fcb0fa39
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/16/2018
ms.locfileid: "51796241"
---
# <a name="ipropertyproxyeesideresolveassemblyref"></a>IPropertyProxyEESide::ResolveAssemblyRef
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

确定指定的托管程序集引用的位置。  
  
## <a name="syntax"></a>语法  
  
```cpp#  
HRESULT ResolveAssemblyRef(  
   BSTR*                  assemName,  
   IEEDataStorage**       assemBytes,  
   IEEDataStorage**       assemPdb,  
   BSTR*                  assemLocation,  
   ASSEMBLYLOCRESOLUTION* alr  
);  
```  
  
```csharp  
int ResolveAssemblyRef(  
   ref string                     assemName,  
   out IEEDataStorage             assemBytes,  
   out IEEDataStorage             assemPdb,  
   out string                     assemLocation,  
   out enum_ASSEMBLYLOCRESOLUTION alr  
);  
```  
  
#### <a name="parameters"></a>参数  
 `assemName`  
 [in]要解析的程序集的名称。  
  
 `assemBytes`  
 [out]返回[IEEDataStorage](../../../extensibility/debugger/reference/ieedatastorage.md)对象，其中包含与引用关联的程序集字节。  
  
 `assemPdb`  
 [out]返回`IEEDataStorage`对象包含的符号存储与此引用关联的数据。  
  
 `assemLocation`  
 [out]返回此引用的路径位置。  
  
 `alr`  
 [out]返回一个值从[ASSEMBLYLOCRESOLUTION](../../../extensibility/debugger/reference/assemblylocresolution.md)枚举，指示此引用的程序集的位置。  
  
## <a name="return-value"></a>返回值  
 如果成功，则返回`S_OK`; 否则为返回错误代码。  
  
## <a name="remarks"></a>备注  
 此方法通常不实现自定义表达式计算器中。  
  
## <a name="see-also"></a>请参阅  
 [IPropertyProxyEESide](../../../extensibility/debugger/reference/ipropertyproxyeeside.md)   
 [IEEDataStorage](../../../extensibility/debugger/reference/ieedatastorage.md)   
 [ASSEMBLYLOCRESOLUTION](../../../extensibility/debugger/reference/assemblylocresolution.md)

