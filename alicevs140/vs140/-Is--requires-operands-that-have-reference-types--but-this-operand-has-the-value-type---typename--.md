---
title: "&#39;Is&#39; requires operands that have reference types, but this operand has the value type &#39;&lt;typename&gt;&#39;"
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
ms.assetid: 228afebd-1203-4bd3-8d7a-c5c56f3cedc4
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Is&#39; requires operands that have reference types, but this operand has the value type &#39;&lt;typename&gt;&#39;
The `Is` comparison operator determines whether two object variables refer to the same instance. This comparison is not defined for value types.  
  
 **Error ID:** BC30020  
  
### To correct this error  
  
-   Use the appropriate arithmetic comparison operator or the `Like` operator to compare two value types.  
  
## See Also  
 [Is Operator](../vs140/Is-Operator--Visual-Basic-.md)   
 [Like Operator](../vs140/Like-Operator--Visual-Basic-.md)   
 [Comparison Operators](../Topic/Comparison%20Operators%20\(Visual%20Basic\).md)