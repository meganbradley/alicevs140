---
title: "&#39;Custom&#39; modifier is not valid on events declared in interfaces"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b5687034-a2b2-4961-88b7-0ba73023573e
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Custom&#39; modifier is not valid on events declared in interfaces
A custom event cannot be declared in an interface because a custom event must provide an implementation of its `AddHandler`, `RemoverHandler`, and `RaiseEvent` methods.  
  
 The `Custom` keyword can be used in a derived class that implements the event.  
  
 **Error ID:** BC31121  
  
### To correct this error  
  
-   Remove the `Custom` keyword from the event declaration in the interface.  
  
## Example  
 This example shows how to implement an event declared in an interface as a custom event.  
  
 [!CODE [VbVbalrEventError#3](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrEventError#3)]  
  
## See Also  
 [Custom - delete](assetId:///dc62be07-c896-4866-a533-982a661d143f)   
 [Event Statement](../vs140/Event-Statement.md)   
 [Delegate Statement](../vs140/Delegate-Statement.md)   
 [Class Statement (Visual Basic)](../Topic/Class%20Statement%20\(Visual%20Basic\).md)   
 [Interface Statement (Visual Basic)](../vs140/Interface-Statement--Visual-Basic-.md)   
 [Events in Visual Basic](../vs140/Events--Visual-Basic-.md)