---
title: "How to: Declare Enumerations (Visual Basic)"
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
ms.assetid: db4ca1c3-f429-4c81-ae81-29e0157b29fd
caps.latest.revision: 26
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Declare Enumerations (Visual Basic)
You create an enumeration with the `Enum` statement in the declarations section of a class or module. You cannot declare an enumeration within a method. To specify the appropriate level of access, use `Private`, `Protected`, `Friend`, or `Public`.  
  
 An `Enum` type has a name, an underlying type, and a set of fields, each representing a constant. The name must be a valid [!INCLUDE[vbprvblong](../vs140/includes/vbprvblong_md.md)] qualifier. The underlying type must be one of the integer types—`Byte`, `Short`, `Long` or `Integer`. `Integer` is the default. Enumerations are always strongly typed and are not interchangeable with integer number types.  
  
 Enumerations cannot have floating-point values. If an enumeration is assigned a floating-point value with `Option Strict On`, a compiler error results. If `Option Strict` is `Off`, the value is automatically converted to the `Enum` type.  
  
 For information on names, and how to use the `Imports` statement to make name qualification unnecessary, see [Enumerations and Name Qualification](../vs140/Enumerations-and-Name-Qualification--Visual-Basic-.md).  
  
### To declare an enumeration  
  
1.  Write a declaration that includes a code access level, the `Enum` keyword, and a valid name, as in the following examples, each of which declares a different `Enum`.  
  
     [!CODE [VbEnumsTask#3](../CodeSnippet/VS_Snippets_VBCSharp/VbEnumsTask#3)]  
  
2.  Define the constants in the enumeration. By default, the first constant in an enumeration is initialized to `0`, and subsequent constants are initialized to a value of one more than the previous constant. For example, the following enumeration, `Days`, contains a constant named `Sunday` with the value `0`, a constant named `Monday` with the value `1`, a constant named `Tuesday` with the value of `2`, and so on.  
  
     [!CODE [VbEnumsTask#4](../CodeSnippet/VS_Snippets_VBCSharp/VbEnumsTask#4)]  
  
3.  You can explicitly assign values to constants in an enumeration by using an assignment statement. You can assign any integer value, including negative numbers. For example, you may want constants with values less than zero to represent error conditions. In the following enumeration, the constant `Invalid` is explicitly assigned the value `–1`, and the constant `Sunday` is assigned the value `0`. Because it is the first constant in the enumeration, `Saturday` is also initialized to the value `0`. The value of `Monday` is `1` (one more than the value of `Sunday`); the value of `Tuesday` is `2`, and so on.  
  
     [!CODE [VbEnumsTask#5](../CodeSnippet/VS_Snippets_VBCSharp/VbEnumsTask#5)]  
  
### To declare an enumeration as an explicit type  
  
-   Specify the type of the enum by using the `As` clause, as shown in the following example.  
  
     [!CODE [VbEnumsTask#6](../CodeSnippet/VS_Snippets_VBCSharp/VbEnumsTask#6)]  
  
## See Also  
 [Enumerations and Name Qualification](../vs140/Enumerations-and-Name-Qualification--Visual-Basic-.md)   
 [How to: Refer to an Enumeration Member](../vs140/How-to--Refer-to-an-Enumeration-Member--Visual-Basic-.md)   
 [How to: Iterate Through An Enumeration in Visual Basic](../Topic/How%20to:%20Iterate%20Through%20An%20Enumeration%20in%20Visual%20Basic.md)   
 [How to: Determine the String Associated with an Enumeration Value](../Topic/How%20to:%20Determine%20the%20String%20Associated%20with%20an%20Enumeration%20Value%20\(Visual%20Basic\).md)   
 [When to Use an Enumeration](../vs140/When-to-Use-an-Enumeration--Visual-Basic-.md)   
 [Constants in Visual Basic](../vs140/Constants-Overview--Visual-Basic-.md)   
 [Constant and Literal Data Types](../vs140/Constant-and-Literal-Data-Types--Visual-Basic-.md)   
 [Constants and Enumerations](../Topic/Constants%20and%20Enumerations%20\(Visual%20Basic\).md)