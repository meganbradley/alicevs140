---
title: "Statement recursively calls the containing &#39;AddHandler&#39; for event &#39;&lt;eventname&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4375b191-fbd9-4e93-b9bb-9159d533ddf6
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Statement recursively calls the containing &#39;AddHandler&#39; for event &#39;&lt;eventname&gt;&#39;
The statements in the `AddHandler` accessor of an event definition must not reference the event directly.  
  
 The recommended approach is to store the list of the event's handlers as a private field in the class, structure, or module that defined the event. For more information, see [How to: Declare Events That Avoid Blocking](../vs140/How-to--Declare-Custom-Events-To-Avoid-Blocking--Visual-Basic-.md) and [How to: Declare Events That Conserve Memory Use](../Topic/How%20to:%20Declare%20Custom%20Events%20To%20Conserve%20Memory%20\(Visual%20Basic\).md).  
  
 **Error ID:** BC41998  
  
### To correct this error  
  
-   Rewrite the event definition to avoid recursion.  
  
## See Also  
 [AddHandler - delete](assetId:///fc464cf8-582c-48a6-a9c2-185c4c3d5ff8)   
 [Event Statement](../vs140/Event-Statement.md)   
 [How to: Declare Events That Avoid Blocking](../vs140/How-to--Declare-Custom-Events-To-Avoid-Blocking--Visual-Basic-.md)   
 [How to: Declare Events That Conserve Memory Use](../Topic/How%20to:%20Declare%20Custom%20Events%20To%20Conserve%20Memory%20\(Visual%20Basic\).md)