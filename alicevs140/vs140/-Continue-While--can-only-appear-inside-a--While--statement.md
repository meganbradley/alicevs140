---
title: "&#39;Continue While&#39; can only appear inside a &#39;While&#39; statement"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b26c77b2-36ae-4dce-b048-f7c4b196faa4
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Continue While&#39; can only appear inside a &#39;While&#39; statement
A `Continue While` statement can only appear within a `For...Next` loop.  
  
 **Error ID:** BC30784  
  
### To correct this error  
  
1.  If the `Continue While` statement is in a `Do...Loop` loop, change the statement to `Continue Do`.  
  
2.  If the `Continue While` statement is in a `For...Next` loop, change the statement to `Continue For`.  
  
3.  Otherwise, remove the `Continue While` statement.  
  
## See Also  
 [Continue Statement (Visual Basic)](../vs140/Continue-Statement--Visual-Basic-.md)   
 [While...End While Statement (Visual Basic)](../Topic/While...End%20While%20Statement%20\(Visual%20Basic\).md)