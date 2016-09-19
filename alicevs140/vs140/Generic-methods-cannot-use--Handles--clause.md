---
title: "Generic methods cannot use &#39;Handles&#39; clause"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 88c62a1c-aee3-46b2-ad78-76790022c04c
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Generic methods cannot use &#39;Handles&#39; clause
A generic `Sub` procedure includes a [Handles](../vs140/Handles-Clause--Visual-Basic-.md) clause in its declaration.  
  
 A `Handles` clause specifies a list of events that the `Sub` procedure handles. To be an event handler, the `Sub` procedure must have the same signature as each event it is to handle. A generic procedure can be created more than once, with signatures that [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] cannot predict at compile time. Therefore, [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] cannot guarantee a signature that matches those of the events in the `Handles` clause.  
  
 **Error ID:** BC32080  
  
### To correct this error  
  
-   If the `Sub` procedure needs to be generic, remove the `Handles` clause from its declaration. Use the [AddHandler Statement](../vs140/AddHandler-Statement.md) to associate this event handler with an event.  
  
-   If the `Sub` procedure needs to use the `Handles` clause to associate events, remove the [Of](../Topic/Of%20Clause%20\(Visual%20Basic\).md) clause from its declaration. You must use a nongeneric procedure with `Handles`.  
  
## See Also  
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [NOT IN BUILD:Events and Event Handlers](assetId:///95074a0d-1cbc-4221-a95a-964185c7f962)