---
title: "How to: Speed Up Access to an Object with a Long Qualification Path (Visual Basic)"
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
ms.assetid: 3eb7657f-c9fe-4e05-8bc3-4bb14d5ae585
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Speed Up Access to an Object with a Long Qualification Path (Visual Basic)
If you frequently access an object that requires a qualification path of several methods and properties, you can speed up your code by not repeating the qualification path.  
  
 There are two ways you can avoid repeating the qualification path. You can assign the object to a variable, or you can use it in a `With`...`End With` block.  
  
### To speed up access to a heavily qualified object by assigning it to a variable  
  
1.  Declare a variable of the type of the object that you are accessing frequently. Specify the qualification path in the initialization part of the declaration.  
  
    ```  
    Dim ctrlActv As Control = someForm.ActiveForm.ActiveControl  
    ```  
  
2.  Use the variable to access the object's members.  
  
    ```  
    ctrlActv.Text = "Test"  
    ctrlActv.Location = New Point(100, 100)  
    ctrlActv.Show()  
    ```  
  
### To speed up access to a heavily qualified object by using a With...End With block  
  
1.  Put the qualification path in a `With` statement.  
  
    ```  
    With someForm.ActiveForm.ActiveControl  
    ```  
  
2.  Access the object's members inside the `With` block, before the `End With` statement.  
  
    ```  
        .Text = "Test"  
        .Location = New Point(100, 100)  
        .Show()  
    End With  
    ```  
  
## See Also  
 [Object Variables in Visual Basic](../Topic/Object%20Variables%20in%20Visual%20Basic.md)   
 [With...End With Statement](../Topic/With...End%20With%20Statement%20\(Visual%20Basic\).md)