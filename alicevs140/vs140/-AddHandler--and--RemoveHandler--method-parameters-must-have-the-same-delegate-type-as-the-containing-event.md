---
title: "&#39;AddHandler&#39; and &#39;RemoveHandler&#39; method parameters must have the same delegate type as the containing event"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 199b2f7b-a85e-465d-9853-0995156e7ab6
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;AddHandler&#39; and &#39;RemoveHandler&#39; method parameters must have the same delegate type as the containing event
A `Custom Event` declaration must have `AddHandler` or `RemoveHandler` declarations, each of which takes a single parameter of the delegate type specified by the custom event's `As` clause.  
  
 **Error ID:** BC31136  
  
### To correct this error  
  
-   Change the type of the parameter to be the same as the delegate type specified by the custom event's `As` clause.  
  
## Example  
 This example shows a custom event with the correct parameter types for the `AddHandler` and `RemoveHandler` declarations.  
  
 [!CODE [VbVbalrEventError#1](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrEventError#1)]  
  
## See Also  
 [Event Statement](../vs140/Event-Statement.md)   
 [AddHandler - delete](assetId:///fc464cf8-582c-48a6-a9c2-185c4c3d5ff8)   
 [RemoveHandler - delete](assetId:///35c17f61-6e22-4b87-b6e1-3ed0c27a88a0)   
 [Events in Visual Basic](../vs140/Events--Visual-Basic-.md)