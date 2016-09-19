---
title: "CAtlServiceModuleT::Handler Function"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 14db5f2a-be87-4774-a296-445cb6fc7b2e
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlServiceModuleT::Handler Function
`CAtlServiceModuleT::Handler` is the routine that the service control manager (SCM) calls to retrieve the status of the service and give it various instructions (such as stopping or pausing). The SCM passes an operation code to `Handler` to indicate what the service should do. A default ATL-generated service only handles the stop instruction. If the SCM passes the stop instruction, the service tells the SCM that the program is about to stop. The service then calls `PostThreadMessage` to post a quit message to itself. This terminates the message loop and the service will ultimately close.  
  
 To handle more instructions, you need to change the `m_status` data member initialized in the `CAtlServiceModuleT` constructor. This data member tells the SCM which buttons to enable when the service is selected in the Services Control Panel application.  
  
## See Also  
 [Services](../vs140/ATL-Services.md)   
 [CAtlServiceModuleT::Handler](../vs140/CAtlServiceModuleT--Handler.md)