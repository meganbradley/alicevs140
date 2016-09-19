---
title: "&#39;AddHandler&#39; or &#39;RemoveHandler&#39; statement event operand must be a dot-qualified expression or a simple name"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b71eb2f0-0bb2-4aeb-94ec-5c37ab960d9e
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;AddHandler&#39; or &#39;RemoveHandler&#39; statement event operand must be a dot-qualified expression or a simple name
The item specified for the event argument to `AddHandler` or `RemoveHandler` is not recognized as an event.  
  
 **Error ID:** BC30677  
  
### To correct this error  
  
-   Specify the name of the object that raises the event followed by a dot (`.`) and the event name as in the following example.  
  
     [!CODE [VbVbalrEventError#30](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrEventError#30)]  
  
## See Also  
 [AddHandler Statement](../vs140/AddHandler-Statement.md)   
 [RemoveHandler Statement](../vs140/RemoveHandler-Statement.md)   
 [NOT IN BUILD:AddHandler and RemoveHandler](assetId:///a7a24bd2-519a-46fe-8a2c-2b9df2ca28ef)   
 [Events in Visual Basic](../vs140/Events--Visual-Basic-.md)