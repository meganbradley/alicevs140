---
title: "Option Strict On disallows operands of type Object for operator &#39;&lt;operatorname&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cd197da8-2676-453b-884b-3231fb6f909d
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Option Strict On disallows operands of type Object for operator &#39;&lt;operatorname&gt;&#39;
Option Strict On disallows operands of type Object for operator '<operatorname\>'. Use the Is operator to test for object identity.  
  
 An arithmetic comparison operator such as `=` is used with one or more object variables when `Option Strict` is `On`.  
  
 **Error ID:** BC32013  
  
### To correct this error  
  
1.  Turn `Option Strict Off` if the object variables contain numeric values and you intend an arithmetic comparison.  
  
2.  Use the `Is` operator to compare for object identity.  
  
## See Also  
 [Comparison Operators](../Topic/Comparison%20Operators%20\(Visual%20Basic\).md)   
 [Is Operator](../vs140/Is-Operator--Visual-Basic-.md)   
 [Option Strict Statement](../vs140/Option-Strict-Statement.md)