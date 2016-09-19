---
title: "&#39;AddressOf&#39; operand must be the name of a method (without parentheses)"
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
ms.assetid: c2c55640-5c61-4e66-97a4-4322020c6001
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;AddressOf&#39; operand must be the name of a method (without parentheses)
The `AddressOf` operator creates a procedure delegate instance that references a specific procedure. The syntax is as follows.  
  
 `AddressOf` `procedurename`  
  
 You inserted parentheses around the argument following `AddressOf`, where none are needed.  
  
 **Error ID:** BC30577  
  
### To correct this error  
  
1.  Remove the parentheses around the argument following `AddressOf`.  
  
2.  Make sure the argument is a method name.  
  
## See Also  
 [AddressOf Operator](../vs140/AddressOf-Operator--Visual-Basic-.md)   
 [Delegates (Visual Basic)](../Topic/Delegates%20\(Visual%20Basic\).md)