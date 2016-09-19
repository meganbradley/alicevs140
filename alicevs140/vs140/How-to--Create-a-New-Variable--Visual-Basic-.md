---
title: "How to: Create a New Variable (Visual Basic)"
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
ms.assetid: 35300be3-77b0-4bef-a156-034d3cdedde0
caps.latest.revision: 31
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Create a New Variable (Visual Basic)
You create a variable with a [Dim Statement (Visual Basic)](../Topic/Dim%20Statement%20\(Visual%20Basic\).md).  
  
### To create a new variable  
  
1.  Declare the variable in a `Dim` statement.  
  
    ```  
  
    Dim newCustomer  
    ```  
  
2.  Include specifications for the variable's characteristics, such as [Private (Visual Basic)](../vs140/Private--Visual-Basic-.md), [Static (Visual Basic)](../vs140/Static--Visual-Basic-.md), [Shadows](../vs140/Shadows--Visual-Basic-.md), or [WithEvents](../vs140/WithEvents--Visual-Basic-.md). For more information, see [Declared Element Characteristics](../vs140/Declared-Element-Characteristics--Visual-Basic-.md).  
  
    ```  
    Public Static newCustomer  
    ```  
  
     You do not need the `Dim` keyword if you use other keywords in the declaration.  
  
3.  Follow the specifications with the variable's name, which must follow [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] rules and conventions. For more information, see [Declared Element Names](../vs140/Declared-Element-Names--Visual-Basic-.md).  
  
    ```  
    Public Static newCustomer  
    ```  
  
4.  Follow the name with the [As](../vs140/As-Clause--Visual-Basic-.md) clause to specify the variable's data type.  
  
    ```  
    Public Static newCustomer As Customer  
    ```  
  
     If you do not specify the data type, it uses the default: `Object`.  
  
5.  Follow the `As` clause with an equal sign (`=`) and follow the equal sign with the variable's initial value.  
  
     [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] assigns the specified value to the variable every time it runs the `Dim` statement. If you do not specify an initial value, [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] assigns the default initial value for the variable's data type when it first enters the code that contains the `Dim` statement.  
  
     If the variable is a reference type, you can create an instance of its class by including the [New (Visual Basic)](../vs140/New-Operator--Visual-Basic-.md) keyword in the `As` clause. If you do not use `New`, the initial value of the variable is [Nothing (Visual Basic)](../Topic/Nothing%20\(Visual%20Basic\).md).  
  
    ```  
    Public Static newCustomer As New Customer  
    ```  
  
## See Also  
 [Variables in Visual Basic](../vs140/Variables-in-Visual-Basic.md)   
 [Variable Declaration in Visual Basic](../Topic/Variable%20Declaration%20in%20Visual%20Basic.md)   
 [Declared Element Names](../vs140/Declared-Element-Names--Visual-Basic-.md)   
 [Declared Element Characteristics](../vs140/Declared-Element-Characteristics--Visual-Basic-.md)   
 [Value Types and Reference Types](../Topic/Value%20Types%20and%20Reference%20Types.md)   
 [Statements (Visual Basic)](../vs140/Statements--Visual-Basic-.md)   
 [Local Type Inference](../vs140/Local-Type-Inference--Visual-Basic-.md)   
 [Option Infer Statement](../vs140/Option-Infer-Statement.md)