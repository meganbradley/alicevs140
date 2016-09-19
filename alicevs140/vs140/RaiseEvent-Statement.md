---
title: "RaiseEvent Statement"
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
ms.assetid: f82e380a-1e6b-4047-bea8-c853f4d2c742
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# RaiseEvent Statement
Triggers an event declared at module level within a class, form, or document.  
  
## Syntax  
  
```  
RaiseEvent eventname[( argumentlist )]  
```  
  
## Parts  
 `eventname`  
 Required. Name of the event to trigger.  
  
 `argumentlist`  
 Optional. Comma-delimited list of variables, arrays, or expressions. The `argumentlist` argument must be enclosed by parentheses. If there are no arguments, the parentheses must be omitted.  
  
## Remarks  
 The required `eventname` is the name of an event declared within the module. It follows Visual Basic variable naming conventions.  
  
 If the event has not been declared within the module in which it is raised, an error occurs. The following code fragment illustrates an event declaration and a procedure in which the event is raised.  
  
 [!CODE [VbVbalrEvents#37](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrEvents#37)]  
  
 You cannot use `RaiseEvent` to raise events that are not explicitly declared in the module. For example, all forms inherit a <xref:System.Windows.Forms.Control.Click?qualifyHint=False> event from <xref:System.Windows.Forms.Form?qualifyHint=True>, it cannot be raised using `RaiseEvent` in a derived form. If you declare a `Click` event in the form module, it shadows the form's own <xref:System.Windows.Forms.Control.Click?qualifyHint=False> event. You can still invoke the form's <xref:System.Windows.Forms.Control.Click?qualifyHint=False> event by calling the <xref:System.Windows.Forms.Control.OnClick?qualifyHint=False> method.  
  
 By default, an event defined in Visual Basic raises its event handlers in the order that the connections are established. Because events can have `ByRef` parameters, a process that connects late may receive parameters that have been changed by an earlier event handler. After the event handlers execute, control is returned to the subroutine that raised the event.  
  
> [!NOTE]
>  Non-shared events should not be raised within the constructor of the class in which they are declared. Although such events do not cause run-time errors, they may fail to be caught by associated event handlers. Use the `Shared` modifier to create a shared event if you need to raise an event from a constructor.  
  
> [!NOTE]
>  You can change the default behavior of events by defining a custom event. For custom events, the `RaiseEvent` statement invokes the event's `RaiseEvent` accessor. For more information on custom events, see [Event Statement](../vs140/Event-Statement.md).  
  
## Example  
 The following example uses events to count down seconds from 10 to 0. The code illustrates several of the event-related methods, properties, and statements, including the `RaiseEvent` statement.  
  
 The class that raises an event is the event source, and the methods that process the event are the event handlers. An event source can have multiple handlers for the events it generates. When the class raises the event, that event is raised on every class that has elected to handle events for that instance of the object.  
  
 The example also uses a form (`Form1`) with a button (`Button1`) and a text box (`TextBox1`). When you click the button, the first text box displays a countdown from 10 to 0 seconds. When the full time (10 seconds) has elapsed, the first text box displays "Done".  
  
 The code for `Form1` specifies the initial and terminal states of the form. It also contains the code executed when events are raised.  
  
 To use this example, open a new Windows Application project, add a button named `Button1` and a text box named `TextBox1` to the main form, named `Form1`. Then right-click the form and click **View Code** to open the Code Editor.  
  
 Add a `WithEvents` variable to the declarations section of the `Form1` class.  
  
 [!CODE [VbVbalrEvents#14](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrEvents#14)]  
  
## Example  
 Add the following code to the code for `Form1`. Replace any duplicate procedures that may exist, such as `Form_Load`, or `Button_Click`.  
  
 [!CODE [VbVbalrEvents#15](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrEvents#15)]  
  
 Press F5 to run the preceding example, and click the button labeled **Start**. The first text box starts to count down the seconds. When the full time (10 seconds) has elapsed, the first text box displays "Done".  
  
> [!NOTE]
>  The `My.Application.DoEvents` method does not process events in exactly the same way as the form does. To allow the form to handle the events directly, you can use multithreading. For more information, see [Threading (C# and Visual Basic)](../vs140/Threading--C#-and-Visual-Basic-.md).  
  
## See Also  
 [Events in Visual Basic](../vs140/Events--Visual-Basic-.md)   
 [Event Statement](../vs140/Event-Statement.md)   
 [AddHandler Statement](../vs140/AddHandler-Statement.md)   
 [RemoveHandler Statement](../vs140/RemoveHandler-Statement.md)   
 [Handles](../vs140/Handles-Clause--Visual-Basic-.md)