---
title: "Handles Clause (Visual Basic)"
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
ms.assetid: 1b051c0e-f499-42f6-acb5-6f4f27824b40
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Handles Clause (Visual Basic)
Declares that a procedure handles a specified event.  
  
## Syntax  
  
```  
  
proceduredeclaration Handles eventlist  
```  
  
## Parts  
 `proceduredeclaration`  
 The `Sub` procedure declaration for the procedure that will handle the event.  
  
 `eventlist`  
 List of the events for `proceduredeclaration` to handle, separated by commas. The events must be raised by either the base class for the current class, or by an object declared using the `WithEvents` keyword.  
  
## Remarks  
 Use the `Handles` keyword at the end of a procedure declaration to cause it to handle events raised by an object variable declared using the `WithEvents` keyword. The `Handles` keyword can also be used in a derived class to handle events from a base class.  
  
 The `Handles` keyword and the `AddHandler` statement both allow you to specify that particular procedures handle particular events, but there are differences. Use the `Handles` keyword when defining a procedure to specify that it handles a particular event. The `AddHandler` statement connects procedures to events at run time. For more information, see [AddHandler Statement](../vs140/AddHandler-Statement.md).  
  
 For custom events, the application invokes the event's `AddHandler` accessor when it adds the procedure as an event handler. For more information on custom events, see [Event Statement](../vs140/Event-Statement.md).  
  
## Example  
 [!CODE [VbVbalrEvents#2](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrEvents#2)]  
  
 The following example demonstrates how a derived class can use the `Handles` statement to handle an event from a base class.  
  
 [!CODE [VbVbalrEvents#3](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrEvents#3)]  
  
## Example  
 The following example contains two button event handlers for a **WPF Application** project.  
  
 [!CODE [VbVbalrEvents#41](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrEvents#41)]  
  
## Example  
 The following example is equivalent to the previous example. The `eventlist` in the `Handles` clause contains the events for both buttons.  
  
 [!CODE [VbVbalrEvents#42](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrEvents#42)]  
  
## See Also  
 [WithEvents](../vs140/WithEvents--Visual-Basic-.md)   
 [AddHandler Statement](../vs140/AddHandler-Statement.md)   
 [RemoveHandler Statement](../vs140/RemoveHandler-Statement.md)   
 [Event Statement](../vs140/Event-Statement.md)   
 [RaiseEvent Statement](../vs140/RaiseEvent-Statement.md)   
 [Events (Visual Basic)](../vs140/Events--Visual-Basic-.md)