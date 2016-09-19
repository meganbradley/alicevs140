---
title: "IsNot Operator (Visual Basic)"
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
ms.assetid: 8dd2bcdb-0166-48a2-9094-60dfb448f36c
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IsNot Operator (Visual Basic)
Compares two object reference variables.  
  
## Syntax  
  
```  
  
result = object1 IsNot object2  
```  
  
## Parts  
 `result`  
 Required. A `Boolean` value.  
  
 `object1`  
 Required. Any `Object` variable or expression.  
  
 `object2`  
 Required. Any `Object` variable or expression.  
  
## Remarks  
 The `IsNot` operator determines if two object references refer to different objects. However, it does not perform value comparisons. If `object1` and `object2` both refer to the exact same object instance, `result` is `False`; if they do not, `result` is `True`.  
  
 `IsNot` is the opposite of the `Is` operator. The advantage of `IsNot` is that you can avoid awkward syntax with `Not` and `Is`, which can be difficult to read.  
  
 You can use the `Is` and `IsNot` operators to test both early-bound and late-bound objects.  
  
> [!NOTE]
>  The `IsNot` operator cannot be used to compare expressions returned from the `TypeOf` operator. Instead, you must use the `Not` and `Is` operators.  
  
## Example  
 The following code example uses both the `Is` operator and the `IsNot` operator to accomplish the same comparison.  
  
 [!CODE [VbVbalrOperators#29](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#29)]  
  
## See Also  
 [Is Operator](../vs140/Is-Operator--Visual-Basic-.md)   
 [TypeOf Operator (Visual Basic)](../Topic/TypeOf%20Operator%20\(Visual%20Basic\).md)   
 [Operator Precedence in Visual Basic](../vs140/Operator-Precedence-in-Visual-Basic.md)   
 [How to: Test Whether Two Objects Are the Same](../vs140/How-to--Test-Whether-Two-Objects-Are-the-Same--Visual-Basic-.md)