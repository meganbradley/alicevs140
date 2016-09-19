---
title: "How to: Declare A Constant (Visual Basic)"
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
ms.assetid: f901b4fa-481f-4621-822e-427060577ad1
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Declare A Constant (Visual Basic)
You use the `Const` statement to declare a constant and set its value. By declaring a constant, you assign a meaningful name to a value. Once a constant is declared, it cannot be modified or assigned a new value.  
  
 You declare a constant within a procedure or in the declarations section of a module, class, or structure. Class or structure-level constants are `Private` by default, but may also be declared as `Public`, `Friend`, `Protected`, or `Protected Friend` for the appropriate level of code access.  
  
 The constant must have a valid symbolic name (the rules are the same as those for creating variable names) and an expression composed of numeric or string constants and operators (but no function calls).  
  
 [!INCLUDE[note_settings_general](../vs140/includes/note_settings_general_md.md)]  
  
### To declare a constant  
  
-   Write a declaration that includes an access specifier, the `Const` keyword, and an expression, as in the following examples:  
  
     [!CODE [VbEnumsTask#8](../CodeSnippet/VS_Snippets_VBCSharp/VbEnumsTask#8)]  
  
     When [Option Infer](../vs140/Option-Infer-Statement.md) is `Off` and [Option Strict](../vs140/Option-Strict-Statement.md) is `On`, you must declare a constant explicitly by specifying a data type (`Boolean`, `Byte`, `Char`, `DateTime`, `Decimal`, `Double`, `Integer`, `Long`, `Short`, `Single`, or `String`).  
  
     When `Option Infer` is `On` or `Option Strict` is `Off`, you can declare a constant without specifying a data type with an `As` clause. The compiler determines the type of the constant from the type of the expression. For more information, see [Constant and Literal Data Types](../vs140/Constant-and-Literal-Data-Types--Visual-Basic-.md).  
  
### To declare a constant that has an explicitly stated data type  
  
-   Write a declaration that includes the `As` keyword and an explicit data type, as in the following examples:  
  
     [!CODE [VbEnumsTask#9](../CodeSnippet/VS_Snippets_VBCSharp/VbEnumsTask#9)]  
  
     You can declare multiple constants on a single line, although your code is more readable if you declare only a single constant per line. If you declare multiple constants on a single line, they must all have the same access level (`Public`, `Private`, `Friend`, `Protected`, or `Protected Friend`).  
  
### To declare multiple constants on a single line  
  
-   Separate the declarations with a comma and a space, as in the following example:  
  
    ```  
    Public Const Four As Integer = 4, Five As Integer = 5, Six As Integer = 44  
    ```  
  
## See Also  
 [Const Statement](../Topic/Const%20Statement%20\(Visual%20Basic\).md)   
 [Constant and Literal Data Types](../vs140/Constant-and-Literal-Data-Types--Visual-Basic-.md)   
 [Constants and Enumerations](../vs140/Constants-and-Enumerations-in-Visual-Basic.md)   
 [Enumerations Overview](../vs140/Enumerations-Overview--Visual-Basic-.md)   
 [Constants Overview (Visual Basic)](../vs140/Constants-Overview--Visual-Basic-.md)   
 [How to: Declare an Enumeration](../vs140/How-to--Declare-Enumerations--Visual-Basic-.md)   
 [Enumerations and Name Qualification](../vs140/Enumerations-and-Name-Qualification--Visual-Basic-.md)   
 [Option Strict Statement](../vs140/Option-Strict-Statement.md)   
 [Constants and Enumerations](../Topic/Constants%20and%20Enumerations%20\(Visual%20Basic\).md)