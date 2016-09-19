---
title: "AndAlso Operator (Visual Basic)"
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
ms.assetid: bbc15191-b374-495b-9b8f-7b8c2f4388eb
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AndAlso Operator (Visual Basic)
Performs short-circuiting logical conjunction on two expressions.  
  
## Syntax  
  
```  
  
result = expression1 AndAlso expression2  
```  
  
## Parts  
  
|||  
|-|-|  
|Term|Definition|  
|`result`|Required. Any `Boolean` expression. The result is the `Boolean` result of comparison of the two expressions.|  
|`expression1`|Required. Any `Boolean` expression.|  
|`expression2`|Required. Any `Boolean` expression.|  
  
## Remarks  
 A logical operation is said to be *short-circuiting* if the compiled code can bypass the evaluation of one expression depending on the result of another expression. If the result of the first expression evaluated determines the final result of the operation, there is no need to evaluate the second expression, because it cannot change the final result. Short-circuiting can improve performance if the bypassed expression is complex, or if it involves procedure calls.  
  
 If both expressions evaluate to `True`, `result` is `True`. The following table illustrates how `result` is determined.  
  
||||  
|-|-|-|  
|If `expression1` is|And `expression2` is|The value of `result` is|  
|`True`|`True`|`True`|  
|`True`|`False`|`False`|  
|`False`|(not evaluated)|`False`|  
  
## Data Types  
 The `AndAlso` operator is defined only for the [Boolean Data Type (Visual Basic)](../vs140/Boolean-Data-Type--Visual-Basic-.md). Visual Basic converts each operand as necessary to `Boolean` and performs the operation entirely in `Boolean`. If you assign the result to a numeric type, Visual Basic converts it from `Boolean` to that type. This could produce unexpected behavior. For example, `5 AndAlso 12` results in `–1` when converted to `Integer`.  
  
## Overloading  
 The [And Operator](../vs140/And-Operator--Visual-Basic-.md) and the [IsFalse Operator](../vs140/IsFalse-Operator--Visual-Basic-.md) can be *overloaded*, which means that a class or structure can redefine their behavior when an operand has the type of that class or structure. Overloading the `And` and `IsFalse` operators affects the behavior of the `AndAlso` operator. If your code uses `AndAlso` on a class or structure that overloads `And` and `IsFalse`, be sure you understand their redefined behavior. For more information, see [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md).  
  
## Example  
 The following example uses the `AndAlso` operator to perform a logical conjunction on two expressions. The result is a `Boolean` value that represents whether the entire conjoined expression is true. If the first expression is `False`, the second is not evaluated.  
  
 [!CODE [VbVbalrOperators#24](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#24)]  
  
 The preceding example produces results of `True`, `False`, and `False`, respectively. In the calculation of `secondCheck`, the second expression is not evaluated because the first is already `False`. However, the second expression is evaluated in the calculation of `thirdCheck`.  
  
## Example  
 The following example shows a `Function` procedure that searches for a given value among the elements of an array. If the array is empty, or if the array length has been exceeded, the `While` statement does not test the array element against the search value.  
  
 [!CODE [VbVbalrOperators#25](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#25)]  
  
## See Also  
 [Logical/Bitwise Operators (Visual Basic)](../vs140/Logical-Bitwise-Operators--Visual-Basic-.md)   
 [Operator Precedence in Visual Basic](../vs140/Operator-Precedence-in-Visual-Basic.md)   
 [Operators Listed by Functionality](../vs140/Operators-Listed-by-Functionality--Visual-Basic-.md)   
 [And Operator](../vs140/And-Operator--Visual-Basic-.md)   
 [IsFalse Operator](../vs140/IsFalse-Operator--Visual-Basic-.md)   
 [Logical and Bitwise Operators in Visual Basic](../vs140/Logical-and-Bitwise-Operators-in-Visual-Basic.md)