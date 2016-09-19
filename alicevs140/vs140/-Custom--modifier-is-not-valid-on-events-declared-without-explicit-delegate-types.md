---
title: "&#39;Custom&#39; modifier is not valid on events declared without explicit delegate types"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6911f0d1-641a-473b-906d-8ee5681194be
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Custom&#39; modifier is not valid on events declared without explicit delegate types
Unlike a non-custom event, a `Custom Event` declaration requires an `As` clause following the event name that explicitly specifies the delegate type for the event.  
  
 Non-custom events can be defined either with an `As` clause and an explicit delegate type, or with a parameter list immediately following the event name.  
  
 **Error ID:** BC31122  
  
### To correct this error  
  
1.  Define a delegate with the same parameter list as the custom event.  
  
     For example, if the `Custom Event` was defined by `Custom Event Test(ByVal sender As Object, ByVal i As Integer)`, then the corresponding delegate would be the following.  
  
     [!CODE [VbVbalrEventError#18](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrEventError#18)]  
  
2.  Replace the parameter list of the custom event with an `As` clause specifying the delegate type.  
  
     Continuing with the example, `Custom Event` declaration would be rewritten as follows.  
  
     [!CODE [VbVbalrEventError#19](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrEventError#19)]  
  
## Example  
 This example declares a `Custom Event` and specifies the required `As` clause with a delegate type.  
  
 [!CODE [VbVbalrEventError#2](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrEventError#2)]  
  
## See Also  
 [Event Statement](../vs140/Event-Statement.md)   
 [Delegate Statement](../vs140/Delegate-Statement.md)   
 [Events in Visual Basic](../vs140/Events--Visual-Basic-.md)