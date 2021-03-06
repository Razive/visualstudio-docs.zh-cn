---
title: 如何：以编程方式发送电子邮件
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- mail items [Office development in Visual Studio], sending e-mail
- Outlook [Office development in Visual Studio], creating e-mail
- Outlook [Office development in Visual Studio], sending e-mail
- e-mail [Office development in Visual Studio], sending
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 91e59cc8d7bd0115a59c71f13e8e2dc200336b29
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/02/2019
ms.locfileid: "53840416"
---
# <a name="how-to-programmatically-send-email"></a>如何：以编程方式发送电子邮件  
  此示例将一封电子邮件发送到具有域的名称的联系人**example.com**电子邮件地址中。  
  
 [!INCLUDE[appliesto_olkallapp](../vsto/includes/appliesto-olkallapp-md.md)]  
  
## <a name="example"></a>示例  
 [!code-csharp[Trin_OL_ProgramEmail#1](../vsto/codesnippet/CSharp/Trin_OL_ProgramEMail/thisaddin.cs#1)]  
  
## <a name="compile-the-code"></a>编译代码  
 此示例需要：  
  
-   具有域的名称的联系人**example.com**电子邮件地址中。  
  
## <a name="robust-programming"></a>可靠编程  
 未删除的域名中搜索的筛选器代码**example.com**。 如果删除筛选器，你的解决方案将向你的联系人的所有发送电子邮件。  
  
## <a name="see-also"></a>请参阅  
 [使用邮件项](../vsto/working-with-mail-items.md)   
 [如何：以编程方式创建电子邮件项](../vsto/how-to-programmatically-create-an-e-mail-item.md)   
 [如何：以编程方式访问 Outlook 联系人](../vsto/how-to-programmatically-access-outlook-contacts.md)   
 [如何：以编程方式执行操作时收到一封电子邮件](../vsto/how-to-programmatically-perform-actions-when-an-e-mail-message-is-received.md)  
