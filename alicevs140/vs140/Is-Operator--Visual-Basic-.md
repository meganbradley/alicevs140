---
title: "Is Operator (Visual Basic)"
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
ms.assetid: 8045a6c8-2a83-45b6-ad47-d09a704c656d
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Is Operator (Visual Basic)
Compares two object reference variables.  
  
## Syntax  
  
```  
  
result = object1 Is object2  
```  
  
## Parts  
 `result`  
 Required. Any `Boolean` value.  
  
 `object1`  
 Required. Any `Object` name.  
  
 `object2`  
 Required. Any `Object` name.  
  
## Remarks  
 The `Is` operator determines if two object references refer to the same object. However, it does not perform value comparisons. If `object1` and `object2` both refer to the exact same object instance, `result` is `True`; if they do not, `result` is `False`.  
  
 `Is` can also be used with the `TypeOf` keyword to make a `TypeOf`...`Is` expression, which tests whether an object variable is compatible with a data type.  
  
> [!NOTE]
>  The `Is` keyword is also used in the [Select...Case Statement (Visual Basic)](../Topic/Select...Case%20Statement%20\(Visual%20Basic\).md).  
  
## Example  
 The following example uses the `Is` operator to compare pairs of object references. The results are assigned to a `Boolean` value representing whether the two objects are identical.  
  
 [!CODE [VbVbalrOperators#27](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#27)]  
  
 As the preceding example demonstrates, you can use the `Is` operator to test both early bound and late bound objects.  
  
## See Also  
 [TypeOf Operator](../Topic/TypeOf%20Operator%20\(Visual%20Basic\).md)   
 [IsNot Operator](../vs140/IsNot-Operator--Visual-Basic-.md)   
 [Comparison Operators in Visual Basic](../vs140/Comparison-Operators-in-Visual-Basic.md)   
 [Operator Precedence in Visual Basic](../vs140/Operator-Precedence-in-Visual-Basic.md)   
 [Operators Listed by Functionality](../vs140/Operators-Listed-by-Functionality--Visual-Basic-.md)   
 [Operators and Expressions](../vs140/Operators-and-Expressions-in-Visual-Basic.md)