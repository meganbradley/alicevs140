---
title: "&amp;= Operator (Visual Basic)"
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
ms.assetid: 0cf262fc-1a05-419a-a503-60013f111c8a
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &amp;= Operator (Visual Basic)
Concatenates a `String` expression to a `String` variable or property and assigns the result to the variable or property.  
  
## Syntax  
  
```  
  
variableorproperty &= expression  
```  
  
## Parts  
 `variableorproperty`  
 Required. Any `String` variable or property.  
  
 `expression`  
 Required. Any `String` expression.  
  
## Remarks  
 The element on the left side of the `&=` operator can be a simple scalar variable, a property, or an element of an array. The variable or property cannot be [ReadOnly (Visual Basic)](../vs140/ReadOnly--Visual-Basic-.md). The `&=` operator concatenates the `String` expression on its right to the `String` variable or property on its left, and assigns the result to the variable or property on its left.  
  
## Overloading  
 The [& Operator](../Topic/&%20Operator%20\(Visual%20Basic\).md) can be *overloaded*, which means that a class or structure can redefine its behavior when an operand has the type of that class or structure. Overloading the `&` operator affects the behavior of the `&=` operator. If your code uses `&=` on a class or structure that overloads `&`, be sure you understand its redefined behavior. For more information, see [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md).  
  
## Example  
 The following example uses the `&=` operator to concatenate two `String` variables and assign the result to the first variable.  
  
 [!CODE [VbVbalrOperators#3](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#3)]  
  
## See Also  
 [& Operator](../Topic/&%20Operator%20\(Visual%20Basic\).md)   
 [+= Operator](../vs140/-=-Operator--Visual-Basic-.md)   
 [Assignment Operators](../vs140/Assignment-Operators--Visual-Basic-.md)   
 [Concatenation Operators](../Topic/Concatenation%20Operators%20\(Visual%20Basic\).md)   
 [Operator Precedence in Visual Basic](../vs140/Operator-Precedence-in-Visual-Basic.md)   
 [Operators Listed by Functionality](../vs140/Operators-Listed-by-Functionality--Visual-Basic-.md)   
 [Statements in Visual Basic](../vs140/Statements-in-Visual-Basic.md)