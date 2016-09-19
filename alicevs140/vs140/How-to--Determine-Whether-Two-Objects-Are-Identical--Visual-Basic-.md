---
title: "How to: Determine Whether Two Objects Are Identical (Visual Basic)"
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
ms.assetid: 7829f817-0d1f-4749-a707-de0b95e0cf5c
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Determine Whether Two Objects Are Identical (Visual Basic)
In [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)], two variable references are considered identical if their pointers are the same, that is, if both variables point to the same class instance in memory. For example, in a Windows Forms application, you might want to make a comparison to determine whether the current instance (`Me`) is the same as a particular instance, such as `Form2`.  
  
 [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] provides two operators to compare pointers. The [Is Operator (Visual Basic)](../vs140/Is-Operator--Visual-Basic-.md) returns `True` if the objects are identical, and the [IsNot Operator](../vs140/IsNot-Operator--Visual-Basic-.md) returns `True` if they are not.  
  
## Determining if Two Objects Are Identical  
  
#### To determine if two objects are identical  
  
1.  Set up a `Boolean` expression to test the two objects.  
  
2.  In your testing expression, use the `Is` operator with the two objects as operands.  
  
     `Is` returns `True` if the objects point to the same class instance.  
  
## Determining if Two Objects Are Not Identical  
 Sometimes you want to perform an action if the two objects are not identical, and it can be awkward to combine `Not` and `Is`, for example `If Not obj1 Is obj2`. In such a case you can use the `IsNot` operator.  
  
#### To determine if two objects are not identical  
  
1.  Set up a `Boolean` expression to test the two objects.  
  
2.  In your testing expression, use the `IsNot` operator with the two objects as operands.  
  
     `IsNot` returns `True` if the objects do not point to the same class instance.  
  
## Example  
 The following example tests pairs of `Object` variables to see if they point to the same class instance.  
  
 [!CODE [VbVbalrKeywords#14](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrKeywords#14)]  
  
 The preceding example displays the following output.  
  
 `objA different from objB? True`  
  
 `objA identical to objC? True`  
  
## See Also  
 [Object Data Type](../Topic/Object%20Data%20Type.md)   
 [Object Variables in Visual Basic](../Topic/Object%20Variables%20in%20Visual%20Basic.md)   
 [Object Variable Values](../Topic/Object%20Variable%20Values%20\(Visual%20Basic\).md)   
 [Is Operator (Visual Basic)](../vs140/Is-Operator--Visual-Basic-.md)   
 [IsNot Operator](../vs140/IsNot-Operator--Visual-Basic-.md)   
 [How to: Determine Whether Two Objects Are Related](../Topic/How%20to:%20Determine%20Whether%20Two%20Objects%20Are%20Related%20\(Visual%20Basic\).md)   
 [Me, My, MyBase, and MyClass in Visual Basic](../vs140/Me--My--MyBase--and-MyClass-in-Visual-Basic.md)