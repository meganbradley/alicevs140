---
title: "User-Defined Constants (Visual Basic)"
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
ms.assetid: a1206d5c-c45e-4ac2-970a-4a0be6a05fdd
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# User-Defined Constants (Visual Basic)
A constant is a meaningful name that takes the place of a number or string that does not change. Constants store values that, as the name implies, remain constant throughout the execution of an application. You can use constants that are defined by the controls or components you work with, or you can create your own. Constants you create yourself are described as *user-defined*.  
  
 You declare a constant with the `Const` statement, using the same guidelines you would for creating a variable name. If `Option Strict` is `On`, you must explicitly declare the constant type.  
  
## Const Statement Usage  
 A `Const` statement can represent a mathematical or date/time quantity:  
  
 [!CODE [VbEnumsTask#10](../CodeSnippet/VS_Snippets_VBCSharp/VbEnumsTask#10)]  
  
 It also can define `String` constants:  
  
 [!CODE [VbEnumsTask#13](../CodeSnippet/VS_Snippets_VBCSharp/VbEnumsTask#13)]  
  
 The expression on the right side of the equal sign ( `=` ) is often a number or literal string, but it also can be an expression that results in a number or string (although that expression cannot contain calls to functions). You can even define constants in terms of previously defined constants:  
  
 [!CODE [VbEnumsTask#15](../CodeSnippet/VS_Snippets_VBCSharp/VbEnumsTask#15)]  
  
## Scope of User-Defined Constants  
 A `Const` statement's scope is the same as that of a variable declared in the same location. You can specify scope in any of the following ways:  
  
-   To create a constant that exists only within a procedure, declare it within that procedure.  
  
-   To create a constant available to all procedures within a class, but not to any code outside that module, declare it in the declarations section of the class.  
  
-   To create a constant that is available to all members of an assembly, but not to outside clients of the assembly, declare it using the `Friend` keyword in the declarations section of the class.  
  
-   To create a constant available throughout the application, declare it using the `Public` keyword in the declarations section the class.  
  
 For more information, see [How to: Declare A Constant](../vs140/How-to--Declare-A-Constant--Visual-Basic-.md).  
  
### Avoiding Circular References  
 Because constants can be defined in terms of other constants, it is possible to inadvertently create a *cycle*, or circular reference, between two or more constants. A cycle occurs when you have two or more public constants, each of which is defined in terms of the other, as in the following example:  
  
 [!CODE [VbEnumsTask#16](../CodeSnippet/VS_Snippets_VBCSharp/VbEnumsTask#16)]  
[!CODE [VbEnumsTask#17](../CodeSnippet/VS_Snippets_VBCSharp/VbEnumsTask#17)]  
  
 If a cycle occurs, [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] generates a compiler error.  
  
## See Also  
 [Const Statement](../Topic/Const%20Statement%20\(Visual%20Basic\).md)   
 [Constant and Literal Data Types](../vs140/Constant-and-Literal-Data-Types--Visual-Basic-.md)   
 [Constants and Enumerations](../vs140/Constants-and-Enumerations-in-Visual-Basic.md)   
 [Constants and Enumerations](../Topic/Constants%20and%20Enumerations%20\(Visual%20Basic\).md)   
 [Enumerations Overview](../vs140/Enumerations-Overview--Visual-Basic-.md)   
 [Constants Overview (Visual Basic)](../vs140/Constants-Overview--Visual-Basic-.md)   
 [How to: Declare an Enumeration](../vs140/How-to--Declare-Enumerations--Visual-Basic-.md)   
 [Enumerations and Name Qualification](../vs140/Enumerations-and-Name-Qualification--Visual-Basic-.md)   
 [Option Strict Statement](../vs140/Option-Strict-Statement.md)