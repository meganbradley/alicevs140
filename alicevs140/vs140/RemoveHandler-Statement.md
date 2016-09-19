---
title: "RemoveHandler Statement"
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
ms.assetid: 647cd825-e877-4910-b4f1-8d168beebe6a
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# RemoveHandler Statement
Removes the association between an event and an event handler.  
  
## Syntax  
  
```  
RemoveHandler event, AddressOf eventhandler  
```  
  
## Parts  
  
|||  
|-|-|  
|Term|Definition|  
|`event`|The name of the event being handled.|  
|`eventhandler`|The name of the procedure currently handling the event.|  
  
## Remarks  
 The `AddHandler` and `RemoveHandler` statements allow you to start and stop event handling for a specific event at any time during program execution.  
  
> [!NOTE]
>  For custom events, the `RemoveHandler` statement invokes the event's `RemoveHandler` accessor. For more information on custom events, see [Event Statement](../vs140/Event-Statement.md).  
  
## Example  
 [!CODE [VbVbalrEvents#17](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrEvents#17)]  
  
## See Also  
 [AddHandler Statement](../vs140/AddHandler-Statement.md)   
 [Handles](../vs140/Handles-Clause--Visual-Basic-.md)   
 [Event Statement](../vs140/Event-Statement.md)   
 [Events (Visual Basic)](../vs140/Events--Visual-Basic-.md)