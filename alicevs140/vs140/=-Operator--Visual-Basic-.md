---
title: "= Operator (Visual Basic)"
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
ms.assetid: 2dac2e49-86c8-42f8-80c1-458452fb5e29
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# = Operator (Visual Basic)
Assigns a value to a variable or property.  
  
## Syntax  
  
```  
  
variableorproperty = value  
```  
  
## Parts  
 `variableorproperty`  
 Any writable variable or any property.  
  
 `value`  
 Any literal, constant, or expression.  
  
## Remarks  
 The element on the left side of the equal sign (`=`) can be a simple scalar variable, a property, or an element of an array. The variable or property cannot be [ReadOnly (Visual Basic)](../vs140/ReadOnly--Visual-Basic-.md). The `=` operator assigns the value on its right to the variable or property on its left.  
  
> [!NOTE]
>  The `=` operator is also used as a comparison operator. For details, see [Comparison Operators (Visual Basic)](../Topic/Comparison%20Operators%20\(Visual%20Basic\).md).  
  
## Overloading  
 The `=` operator can be overloaded only as a relational comparison operator, not as an assignment operator. For more information, see [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md).  
  
## Example  
 The following example demonstrates the assignment operator. The value on the right is assigned to the variable on the left.  
  
 [!CODE [VbVbalrOperators#9](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#9)]  
  
## See Also  
 [&= Operator](../vs140/-=-Operator--Visual-Basic-.md)   
 [*= Operator](../vs140/-=-Operator--Visual-Basic-.md)   
 [+= Operator](../vs140/-=-Operator--Visual-Basic-.md)   
 [-= Operator (Visual Basic)](../vs140/-=-Operator--Visual-Basic-2.md)   
 [/= Operator (Visual Basic)](../vs140/-=-Operator--Visual-Basic-1.md)   
 [\\= Operator](../vs140/-=-Operator.md)   
 [^= Operator](../vs140/^=-Operator--Visual-Basic-.md)   
 [Statements in Visual Basic](../vs140/Statements-in-Visual-Basic.md)   
 [Comparison Operators (Visual Basic)](../Topic/Comparison%20Operators%20\(Visual%20Basic\).md)   
 [ReadOnly (Visual Basic)](../vs140/ReadOnly--Visual-Basic-.md)   
 [Local Type Inference](../vs140/Local-Type-Inference--Visual-Basic-.md)