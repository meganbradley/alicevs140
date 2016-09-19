---
title: "MAPI"
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
ms.assetid: 193449f7-b131-4ab0-9301-8d4f6cd1e7c4
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MAPI
This article describes the Microsoft Messaging Application Programming Interface (MAPI) for client message application developers. MFC supplies support for a subset of MAPI in class **CDocument** but does not encapsulate the entire API. For more information, see [MAPI Support in MFC](../vs140/MAPI-Support-in-MFC.md).  
  
 MAPI is a set of functions that mail-enabled and mail-aware applications use to create, manipulate, transfer, and store mail messages. It gives application developers the tools to define the purpose and content of mail messages and gives them flexibility in their management of stored mail messages. MAPI also provides a common interface that application developers can use to create mail-enabled and mail-aware applications independent of the underlying messaging system.  
  
 Messaging clients provide a human interface for interaction with the Microsoft Windows Messaging System (WMS). This interaction typically includes requesting services from MAPI-compliant providers such as message stores and address books.  
  
 For more information about MAPI, see the articles under Guide in Win32 Messaging (MAPI) of the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## In This Section  
 [MAPI Support in MFC](../vs140/MAPI-Support-in-MFC.md)  
  
## See Also  
 [CDocument::OnFileSendMail](../vs140/CDocument--OnFileSendMail.md)   
 [CDocument::OnUpdateFileSendMail](../vs140/CDocument--OnUpdateFileSendMail.md)   
 [COleDocument::OnFileSendMail](../vs140/COleDocument--OnFileSendMail.md)