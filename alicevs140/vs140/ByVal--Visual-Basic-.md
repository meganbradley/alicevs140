---
title: "ByVal (Visual Basic)"
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
ms.assetid: 1eaf4e58-b305-4785-9e3d-e416b9c75598
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ByVal (Visual Basic)
Specifies that an argument is passed in such a way that the called procedure or property cannot change the value of a variable underlying the argument in the calling code.  
  
## Remarks  
 The `ByVal` modifier can be used in these contexts:  
  
 [Declare Statement](../Topic/Declare%20Statement.md)  
  
 [Function Statement](../Topic/Function%20Statement%20\(Visual%20Basic\).md)  
  
 [Operator Statement](../vs140/Operator-Statement.md)  
  
 [Property Statement](../vs140/Property-Statement.md)  
  
 [Sub Statement](../Topic/Sub%20Statement%20\(Visual%20Basic\).md)  
  
## Example  
 The following example demonstrates the use of the `ByVal` parameter passing mechanism with a reference type argument. In the example, the argument is `c1`, an instance of class `Class1`. `ByVal` prevents the code in the procedures from changing the underlying value of the reference argument, `c1`, but does not protect the accessible fields and properties of `c1`.  
  
 [!CODE [VbVbalrKeywords#10](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrKeywords#10)]  
  
## See Also  
 [Keywords (Visual Basic)](../vs140/Keywords--Visual-Basic-.md)   
 [Passing Arguments by Value and by Reference](../vs140/Passing-Arguments-by-Value-and-by-Reference--Visual-Basic-.md)