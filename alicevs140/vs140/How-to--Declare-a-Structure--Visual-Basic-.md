---
title: "How to: Declare a Structure (Visual Basic)"
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
ms.assetid: d5e98381-eb81-47d4-af83-48cc534a2572
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Declare a Structure (Visual Basic)
You begin a structure declaration with the [Structure Statement](../Topic/Structure%20Statement.md), and you end it with the `End` `Structure` statement. Between these two statements you must declare at least one *element*. The elements can be of any data type, but at least one must be either a nonshared variable or a nonshared, noncustom event.  
  
 You cannot initialize any of the structure elements in the structure declaration. When you declare a variable to be of a structure type, you assign values to the elements by accessing them through the variable.  
  
 For a discussion of the differences between structures and classes, see [Structures and Classes](../Topic/Structures%20and%20Classes%20\(Visual%20Basic\).md).  
  
 For demonstration purposes, consider a situation where you want to keep track of an employee's name, telephone extension, and salary. A structure allows you to do this in a single variable.  
  
### To declare a structure  
  
1.  Create the beginning and ending statements for the structure.  
  
     You can specify the access level of a structure using the [Public (Visual Basic)](../vs140/Public--Visual-Basic-.md), [Protected (Visual Basic)](../vs140/Protected--Visual-Basic-.md), [Friend (Visual Basic)](../Topic/Friend%20\(Visual%20Basic\).md), or [Private (Visual Basic)](../vs140/Private--Visual-Basic-.md) keyword, or you can let it default to `Public`.  
  
    ```  
    Private Structure employee  
    End Structure  
    ```  
  
2.  Add elements to the body of the structure.  
  
     A structure must have at least one element. You must declare every element and specify an access level for it. If you use the [Dim Statement (Visual Basic)](../Topic/Dim%20Statement%20\(Visual%20Basic\).md) without any keywords, the accessibility defaults to `Public`.  
  
    ```  
    Private Structure employee  
        Public givenName As String  
        Public familyName As String  
        Public phoneExtension As Long  
        Private salary As Decimal  
        Public Sub giveRaise(raise As Double)  
            salary *= raise  
        End Sub  
        Public Event salaryReviewTime()  
    End Structure  
    ```  
  
     The `salary` field in the preceding example is `Private`, which means it is inaccessible outside the structure, even from the containing class. However, the `giveRaise` procedure is `Public`, so it can be called from outside the structure. Similarly, you can raise the `salaryReviewTime` event from outside the structure.  
  
     In addition to variables, `Sub` procedures, and events, you can also define constants, `Function` procedures, and properties in a structure. You can designate at most one property as the *default property*, provided it takes at least one argument. You can handle an event with a [Shared (Visual Basic)](../Topic/Shared%20(Visual%20Basic).md)`Sub` procedure. For more information, see [How to: Declare and Call a Default Property in Visual Basic](../Topic/How%20to:%20Declare%20and%20Call%20a%20Default%20Property%20in%20Visual%20Basic.md).  
  
## See Also  
 [Data Types in Visual Basic](../vs140/Data-Types-in-Visual-Basic.md)   
 [Elementary Data Types](../vs140/Elementary-Data-Types--Visual-Basic-.md)   
 [Composite Data Types](../vs140/Composite-Data-Types--Visual-Basic-.md)   
 [Value Types and Reference Types](../Topic/Value%20Types%20and%20Reference%20Types.md)   
 [Structures: Your Own Data Types](../vs140/Structures--Visual-Basic-.md)   
 [Troubleshooting Data Types](../Topic/Troubleshooting%20Data%20Types%20\(Visual%20Basic\).md)   
 [Structure Variables](../vs140/Structure-Variables--Visual-Basic-.md)   
 [Structures and Other Programming Elements](../vs140/Structures-and-Other-Programming-Elements--Visual-Basic-.md)   
 [Structures and Classes](../Topic/Structures%20and%20Classes%20\(Visual%20Basic\).md)   
 [User-Defined Data Type](../vs140/User-Defined-Data-Type.md)