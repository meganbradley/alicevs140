---
title: "&#39;Return&#39; statement in an &#39;AddHandler&#39;, &#39;RemoveHandler&#39;, or &#39;RaiseEvent&#39; method cannot return a value"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0e4d037a-2d20-40e4-8ead-6d709d1c9c7a
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Return&#39; statement in an &#39;AddHandler&#39;, &#39;RemoveHandler&#39;, or &#39;RaiseEvent&#39; method cannot return a value
The `AddHandler`, `RemoveHandler`, and `RaiseEvent` methods in a `Custom Event` declaration can contain `Return` statements to exit the methods. However, the `Return` statement cannot specify a return value because the methods cannot return values.  
  
 **Error ID:** BC30940  
  
### To correct this error  
  
-   Remove the expression following the `Return` statement.  
  
## See Also  
 [Event Statement](../vs140/Event-Statement.md)   
 [AddHandler - delete](assetId:///fc464cf8-582c-48a6-a9c2-185c4c3d5ff8)   
 [RemoveHandler - delete](assetId:///35c17f61-6e22-4b87-b6e1-3ed0c27a88a0)   
 [RaiseEvent - delete](assetId:///7f765da0-5491-40b6-9ed5-24c98f9daad9)   
 [Return Statement (Visual Basic)](../vs140/Return-Statement--Visual-Basic-.md)   
 [Events in Visual Basic](../vs140/Events--Visual-Basic-.md)