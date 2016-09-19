---
title: "Statement does not declare an &#39;AddHandler&#39;, &#39;RemoveHandler&#39; or &#39;RaiseEvent&#39; method"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f8299c9d-6030-43e5-878e-8d2b042191b5
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Statement does not declare an &#39;AddHandler&#39;, &#39;RemoveHandler&#39; or &#39;RaiseEvent&#39; method
The statement does not supply an `AddHandler`, `RemoveHandler`, or `RaiseEvent` declaration statement around a `Custom Event` procedure. A custom event declaration is a block of code enclosed within the `Custom Event` and `End Event` statements. Inside this block, each `Custom Event` procedure appears as an internal block enclosed within a declaration statement and an `End` statement.  
  
 **Error ID:** BC31113  
  
### To correct this error  
  
-   Supply an `AddHandler`, `RemoveHandler`, or `RaiseEvent` declaration statement.  
  
## See Also  
 [Event Statement](../vs140/Event-Statement.md)   
 [AddHandler - delete](assetId:///fc464cf8-582c-48a6-a9c2-185c4c3d5ff8)   
 [RemoveHandler - delete](assetId:///35c17f61-6e22-4b87-b6e1-3ed0c27a88a0)   
 [RaiseEvent - delete](assetId:///7f765da0-5491-40b6-9ed5-24c98f9daad9)   
 [Events in Visual Basic](../vs140/Events--Visual-Basic-.md)