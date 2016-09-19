---
title: "How to: Group Related Constant Values Together (Visual Basic)"
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
ms.assetid: 09d61da5-c940-4126-a79f-ba93c36653dc
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Group Related Constant Values Together (Visual Basic)
An enumeration is the best way to group related constants together. You create an enumeration with the `Enum` statement in the declarations section of a class or a module. For more information, see [How to: Declare Enumerations](../vs140/How-to--Declare-Enumerations--Visual-Basic-.md).  
  
### To group related constant values  
  
1.  Write a declaration that includes a code access level, the `Enum` keyword, and a valid name. This example creates the `Private` enumeration, `temperatureValues`.  
  
     [!CODE [VbEnumsTask#21](../CodeSnippet/VS_Snippets_VBCSharp/VbEnumsTask#21)]  
  
2.  Define the constants in the enumeration. This example creates the `Public` enumeration `temperatureValues` and assigns its values.  
  
     [!CODE [VbEnumsTask#1](../CodeSnippet/VS_Snippets_VBCSharp/VbEnumsTask#1)]  
  
## See Also  
 [Enumerations and Name Qualification](../vs140/Enumerations-and-Name-Qualification--Visual-Basic-.md)   
 [How to: Refer to an Enumeration Member](../vs140/How-to--Refer-to-an-Enumeration-Member--Visual-Basic-.md)   
 [When to Use an Enumeration](../vs140/When-to-Use-an-Enumeration--Visual-Basic-.md)   
 [Constants Overview (Visual Basic)](../vs140/Constants-Overview--Visual-Basic-.md)   
 [Constant and Literal Data Types](../vs140/Constant-and-Literal-Data-Types--Visual-Basic-.md)   
 [Constants and Enumerations](../Topic/Constants%20and%20Enumerations%20\(Visual%20Basic\).md)