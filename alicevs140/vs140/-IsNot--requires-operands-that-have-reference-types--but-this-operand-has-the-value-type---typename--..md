---
title: "&#39;IsNot&#39; requires operands that have reference types, but this operand has the value type &#39;&lt;typename&gt;&#39;."
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c44d2936-8c07-443a-b320-ac2bfbc1e9ec
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;IsNot&#39; requires operands that have reference types, but this operand has the value type &#39;&lt;typename&gt;&#39;.
An expression uses the [IsNot Operator](../vs140/IsNot-Operator--Visual-Basic-.md) with at least one value type operand.  
  
 The `IsNot` operator determines whether two object references refer to different objects. It compares the pointer values of reference types and is meaningless with value types.  
  
 **Error ID:** BC31419  
  
### To correct this error  
  
-   If you intend to compare the values of two value types, use the `=` or `<>` comparison operator.  
  
-   If you intend to compare the pointers of two reference types, be sure you are using object references for both operands. You can use reference variables or elements, such as the [Me](assetId:///a65973c7-cf06-4547-9b25-9fba885525c2) keyword, that behave like reference variables.  
  
## See Also  
 [Comparison Operators in Visual Basic](../vs140/Comparison-Operators-in-Visual-Basic.md)   
 [How to: Test Whether Two Objects Are the Same](../vs140/How-to--Test-Whether-Two-Objects-Are-the-Same--Visual-Basic-.md)