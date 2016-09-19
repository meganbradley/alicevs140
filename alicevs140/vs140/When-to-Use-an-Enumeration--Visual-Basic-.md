---
title: "When to Use an Enumeration (Visual Basic)"
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
ms.assetid: e6e47b5b-3ed9-452d-a481-9c3fed88519a
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# When to Use an Enumeration (Visual Basic)
Enumerations offer an easy way to work with sets of related constants. An enumeration, or `Enum`, is a symbolic name for a set of values. Enumerations are treated as data types, and you can use them to create sets of constants for use with variables and properties.  
  
## When to Use an Enumeration  
 Whenever a procedure accepts a limited set of variables, consider using an enumeration. Enumerations make for clearer and more readable code, particularly when meaningful names are used.  
  
 The benefits of using enumerations include:  
  
-   Reduces errors caused by transposing or mistyping numbers.  
  
-   Makes it easy to change values in the future.  
  
-   Makes code easier to read, which means it is less likely that errors will creep into it.  
  
-   Ensures forward compatibility. With enumerations, your code is less likely to fail if in the future someone changes the values corresponding to the member names.  
  
## Naming Enumerations  
 Use a naming convention for enumeration members. When [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] encounters an enumeration member name, an exception may be thrown if other referenced type libraries contain the same name. Use a unique prefix that identifies the values from your application or component.  
  
 When referring to a member of an enumeration, you must qualify the member name with the enumeration name or else use the `Imports` statement. For more information, see [Enumerations and Name Qualification](../vs140/Enumerations-and-Name-Qualification--Visual-Basic-.md).  
  
## Predefined Enumerations  
 [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] provides a number of predefined enumerations, such as `FirstDayOfWeek` and `MsgBoxResul`t, to facilitate your code. For a list of these see [Constants and Enumerations (Visual Basic)](../Topic/Constants%20and%20Enumerations%20\(Visual%20Basic\).md).  
  
## See Also  
 [How to: Declare Enumerations](../vs140/How-to--Declare-Enumerations--Visual-Basic-.md)   
 [How to: Refer to an Enumeration Member](../vs140/How-to--Refer-to-an-Enumeration-Member--Visual-Basic-.md)   
 [Enumerations and Name Qualification](../vs140/Enumerations-and-Name-Qualification--Visual-Basic-.md)   
 [How to: Iterate Through An Enumeration in Visual Basic](../Topic/How%20to:%20Iterate%20Through%20An%20Enumeration%20in%20Visual%20Basic.md)   
 [How to: Determine the String Associated with an Enumeration Value](../Topic/How%20to:%20Determine%20the%20String%20Associated%20with%20an%20Enumeration%20Value%20\(Visual%20Basic\).md)   
 [Enum Statement (Visual Basic)](../Topic/Enum%20Statement%20\(Visual%20Basic\).md)   
 [Constants and Enumerations](../Topic/Constants%20and%20Enumerations%20\(Visual%20Basic\).md)