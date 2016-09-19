---
title: "Operator &#39;&lt;operator&gt;&#39; must have a return type of Boolean"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 18e066f4-d71e-4e38-b0bc-8af9145f6015
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Operator &#39;&lt;operator&gt;&#39; must have a return type of Boolean
A comparison or logical operator is declared with a return type other than the [Boolean Data Type (Visual Basic)](../vs140/Boolean-Data-Type--Visual-Basic-.md).  
  
 The result of a comparison operator (`=`, `<>`, `<`, `<=`, `>`, `>=`, `Is`, `IsNot`, `IsFalse`, `IsTrue`, `Like`, `TypeOf`) can be only `True` or `False`. For more information, see [Comparison Operators in Visual Basic](../vs140/Comparison-Operators-in-Visual-Basic.md).  
  
 Logical operators (`And`, `AndAlso`, `Not`, `Or`, `OrElse`, `Xor`) work entirely within the domain of Boolean values. For more information, see [Logical Operators in Visual Basic](../vs140/Logical-and-Bitwise-Operators-in-Visual-Basic.md).  
  
 **Error ID:** BC33023  
  
### To correct this error  
  
-   Replace the return type of this comparison or logical operator with `Boolean`.  
  
## See Also  
 [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md)   
 [Operator Statement](../vs140/Operator-Statement.md)   
 [How to: Define an Operator](../vs140/How-to--Define-an-Operator--Visual-Basic-.md)   
 [How to: Define a Conversion Operator](../vs140/How-to--Define-a-Conversion-Operator--Visual-Basic-.md)