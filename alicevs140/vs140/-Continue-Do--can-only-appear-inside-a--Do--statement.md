---
title: "&#39;Continue Do&#39; can only appear inside a &#39;Do&#39; statement"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c6b35e63-4d84-449d-9685-41a1bc0a7f35
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Continue Do&#39; can only appear inside a &#39;Do&#39; statement
A `Continue Do` statement can only appear within a `Do...Loop` loop.  
  
 **Error ID:** BC30782  
  
### To correct this error  
  
1.  If the `Continue Do` statement is in a `For...Next` loop, change the statement to `Continue For`.  
  
2.  If the `Continue Do` statement is in a `While...End While` loop, change the statement to `Continue While`.  
  
3.  Otherwise, remove the `Continue Do` statement.  
  
## See Also  
 [Continue Statement (Visual Basic)](../vs140/Continue-Statement--Visual-Basic-.md)   
 [Do...Loop Statement (Visual Basic)](../vs140/Do...Loop-Statement--Visual-Basic-.md)