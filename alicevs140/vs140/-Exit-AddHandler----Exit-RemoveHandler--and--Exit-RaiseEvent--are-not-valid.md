---
title: "&#39;Exit AddHandler&#39;, &#39;Exit RemoveHandler&#39; and &#39;Exit RaiseEvent&#39; are not valid"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e02264f3-0645-4de5-b622-8a2a74496b64
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Exit AddHandler&#39;, &#39;Exit RemoveHandler&#39; and &#39;Exit RaiseEvent&#39; are not valid
'Exit AddHandler', 'Exit RemoveHandler' and 'Exit RaiseEvent' are not valid. Use 'Return' to exit from event members.  
  
 The `Exit` statement cannot be used to exit `AddHandler`, `RemoveHandler`, or `RaiseEvent` methods in a `Custom Event` declaration. Instead, use the `Return` statement, without specifying a return expression, to exit the method.  
  
 **Error ID:** BC31111  
  
### To correct this error  
  
-   Replace the `Exit` statement with a `Return` statement.  
  
     Make sure the `Return` statement does not specify a return expression.  
  
## See Also  
 [Event Statement](../vs140/Event-Statement.md)   
 [AddHandler - delete](assetId:///fc464cf8-582c-48a6-a9c2-185c4c3d5ff8)   
 [RemoveHandler - delete](assetId:///35c17f61-6e22-4b87-b6e1-3ed0c27a88a0)   
 [RaiseEvent - delete](assetId:///7f765da0-5491-40b6-9ed5-24c98f9daad9)   
 [Return Statement (Visual Basic)](../vs140/Return-Statement--Visual-Basic-.md)   
 [Events in Visual Basic](../vs140/Events--Visual-Basic-.md)