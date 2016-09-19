---
title: "&#39;#Else&#39; must be preceded by a matching &#39;#If&#39; or &#39;#ElseIf&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c6ed34de-d6ed-4227-9880-538055aff20a
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;#Else&#39; must be preceded by a matching &#39;#If&#39; or &#39;#ElseIf&#39;
`#Else` is a conditional compilation directive. An `#Else` directive is not preceded by a corresponding `#If` or `#ElseIf` directive.  
  
 **Error ID:** BC30028  
  
### To correct this error  
  
1.  Check that a preceding `#If` or `#ElseIf` is not separated from this `#Else` by an intervening conditional compilation block or an incorrectly placed `#End If`.  
  
2.  Check that `#Else` is preceded by another `#Else` directive. If it is, either remove `#Else` or change it to an `#ElseIf`.  
  
3.  If everything else is in order, add an `#If` directive to the beginning of the conditional compilation block.  
  
## See Also  
 [#If...Then...#Else Directives](../vs140/#If...Then...#Else-Directives.md)