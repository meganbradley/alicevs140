---
title: "Walkthrough: Creating and Implementing Interfaces (Visual Basic)"
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
ms.assetid: ded82af2-9f52-4232-98ef-fe458180f112
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Walkthrough: Creating and Implementing Interfaces (Visual Basic)
Interfaces describe the characteristics of properties, methods, and events, but leave the implementation details up to structures or classes.  
  
 This walkthrough demonstrates how to declare and implement an interface.  
  
> [!NOTE]
>  This walkthrough doesn't provide information about how to create a user interface.  
  
 [!INCLUDE[note_settings_general](../vs140/includes/note_settings_general_md.md)]  
  
### To define an interface  
  
1.  Open a new [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] Windows Application project.  
  
2.  Add a new module to the project by clicking **Add Module** on the **Project** menu.  
  
3.  Name the new module `Module1.vb` and click **Add**. The code for the new module is displayed.  
  
4.  Define an interface named `TestInterface` within `Module1` by typing `Interface TestInterface` between the `Module` and `End Module` statements, and then pressing ENTER. The **Code Editor** indents the `Interface` keyword and adds an `End Interface` statement to form a code block.  
  
5.  Define a property, method, and event for the interface by placing the following code between the `Interface` and `End Interface` statements:  
  
     [!CODE [VbVbalrOOP#98](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOOP#98)]  
  
## Implementation  
 You may notice that the syntax used to declare interface members is different from the syntax used to declare class members. This difference reflects the fact that interfaces cannot contain implementation code.  
  
#### To implement the interface  
  
1.  Add a class named `ImplementationClass` by adding the following statement to `Module1`, after the `End Interface` statement but before the `End Module` statement, and then pressing ENTER:  
  
     [!CODE [VbVbalrOOP#99](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOOP#99)]  
  
     If you are working within the integrated development environment, the **Code Editor** supplies a matching `End Class` statement when you press ENTER.  
  
2.  Add the following `Implements` statement to `ImplementationClass`, which names the interface the class implements:  
  
     [!CODE [VbVbalrOOP#100](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOOP#100)]  
  
     When listed separately from other items at the top of a class or structure, the `Implements` statement indicates that the class or structure implements an interface.  
  
     If you are working within the integrated development environment, the **Code Editor** implements the class members required by `TestInterface` when you press ENTER, and you can skip the next step.  
  
3.  If you are not working within the integrated development environment, you must implement all the members of the interface `MyInterface`. Add the following code to `ImplementationClass` to implement `Event1`, `Method1`, and `Prop1`:  
  
     [!CODE [VbVbalrOOP#101](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOOP#101)]  
  
     The `Implements` statement names the interface and interface member being implemented.  
  
4.  Complete the definition of `Prop1` by adding a private field to the class that stored the property value:  
  
     [!CODE [VbVbalrOOP#102](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOOP#102)]  
  
     Return the value of the `pval` from the property get accessor.  
  
     [!CODE [VbVbalrOOP#103](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOOP#103)]  
  
     Set the value of `pval` in the property set accessor.  
  
     [!CODE [VbVbalrOOP#104](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOOP#104)]  
  
5.  Complete the definition of `Method1` by adding the following code.  
  
     [!CODE [VbVbalrOOP#105](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOOP#105)]  
  
#### To test the implementation of the interface  
  
1.  Right-click the startup form for your project in the **Solution Explorer**, and click **View Code**. The editor displays the class for your startup form. By default, the startup form is called `Form1`.  
  
2.  Add the following `testInstance` field to the `Form1` class:  
  
     [!CODE [VbVbalrOOP#120](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOOP#120)]  
  
     By declaring `testInstance` as `WithEvents`, the `Form1` class can handle its events.  
  
3.  Add the following event handler to the `Form1` class to handle events raised by `testInstance`:  
  
     [!CODE [VbVbalrOOP#106](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOOP#106)]  
  
4.  Add a subroutine named `Test` to the `Form1` class to test the implementation class:  
  
     [!CODE [VbVbalrOOP#107](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOOP#107)]  
  
     The `Test` procedure creates an instance of the class that implements `MyInterface`, assigns that instance to the `testInstance` field, sets a property, and runs a method through the interface.  
  
5.  Add code to call the `Test` procedure from the `Form1 Load` procedure of your startup form:  
  
     [!CODE [VbVbalrOOP#108](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOOP#108)]  
  
6.  Run the `Test` procedure by pressing F5. The message "Prop1 was set to 9" is displayed. After you click OK, the message "The X parameter for Method1 is 5" is displayed. Click OK, and the message "The event handler caught the event" is displayed.  
  
## See Also  
 [Implements Statement](../vs140/Implements-Statement.md)   
 [Interfaces](../vs140/Interfaces--Visual-Basic-.md)   
 [Interface Statement](../vs140/Interface-Statement--Visual-Basic-.md)   
 [Event Statement](../vs140/Event-Statement.md)