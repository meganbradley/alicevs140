---
title: "Walkthrough: Defining Classes (Visual Basic)"
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
ms.assetid: 07018828-2d49-4cf5-a44b-19fb15d9efea
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Walkthrough: Defining Classes (Visual Basic)
This walkthrough demonstrates how to define classes, which you can then use to create objects. It also shows you how to add properties and methods to the new class, and demonstrates how to initialize an object.  
  
 [!INCLUDE[note_settings_general](../vs140/includes/note_settings_general_md.md)]  
  
### To define a class  
  
1.  Create a project by clicking **New Project** on the **File** menu. The **New Project** dialog box appears.  
  
2.  Select Windows Application from the list of [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] project templates to display the new project.  
  
3.  Add a new class to the project by clicking **Add Class** on the **Project** menu. The **Add New Item** dialog box appears.  
  
4.  Select the **Class** template.  
  
5.  Name the new class `UserNameInfo.vb`, and then click **Add** to display the code for the new class.  
  
     [!CODE [VbVbalrOOP#5](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOOP#5)]  
  
    > [!NOTE]
    >  You can use the [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] **Code Editor** to add a class to your startup form by typing the `Class` keyword followed by the name of the new class. The **Code Editor** provides a corresponding `End Class` statement for you.  
  
6.  Define a private field for the class by adding the following code between the `Class` and `End Class` statements:  
  
     [!CODE [VbVbalrOOP#7](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOOP#7)]  
  
     Declaring the field as `Private` means it can be used only within the class. You can make fields available from outside a class by using access modifiers such as `Public` that provide more access. For more information, see [Access Levels in Visual Basic](../vs140/Access-Levels-in-Visual-Basic.md).  
  
7.  Define a property for the class by adding the following code:  
  
     [!CODE [VbVbalrOOP#8](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOOP#8)]  
  
8.  Define a method for the class by adding the following code:  
  
     [!CODE [VbVbalrOOP#9](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOOP#9)]  
  
9. Define a parameterized constructor for the new class by adding a procedure named `Sub New`:  
  
     [!CODE [VbVbalrOOP#10](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOOP#10)]  
  
     The `Sub New` constructor is called automatically when an object based on this class is created. This constructor sets the value of the field that holds the user name.  
  
### To create a button to test the class  
  
1.  Change the startup form to design mode by right-clicking its name in **Solution Explorer** and then clicking **View Designer**. By default, the startup form for Windows Application projects is named Form1.vb. The main form will then appear.  
  
2.  Add a button to the main form and double-click it to display the code for the `Button1_Click` event handler. Add the following code to call the test procedure:  
  
     [!CODE [VbVbalrOOP#12](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOOP#12)]  
  
### To run your application  
  
1.  Run your application by pressing F5. Click the button on the form to call the test procedure. It displays a message stating that the original `UserName` is "MOORE, BOBBY", because the procedure called the `Capitalize` method of the object.  
  
2.  Click **OK** to dismiss the message box. The `Button1 Click` procedure changes the value of the `UserName` property and displays a message stating that the new value of `UserName` is "Worden, Joe".  
  
## See Also  
 [Object-Oriented Programming with Managed Languages](../vs140/Object-Oriented-Programming--C#-and-Visual-Basic-.md)   
 [Objects and Classes in Visual Basic](../Topic/Objects%20and%20Classes%20in%20Visual%20Basic.md)