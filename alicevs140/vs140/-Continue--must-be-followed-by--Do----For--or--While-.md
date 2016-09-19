---
title: "&#39;Continue&#39; must be followed by &#39;Do&#39;, &#39;For&#39; or &#39;While&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a0d5854d-ca44-4c6b-9458-4fc50d29281a
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Continue&#39; must be followed by &#39;Do&#39;, &#39;For&#39; or &#39;While&#39;
A `Continue` statement must be followed by `Do`, `For`, or `While`, depending on if the `Continue` statement appears within a `Do...Loop` loop, `For...Next` loop, or `While...End While` loop.  
  
 **Error ID:** BC30781  
  
### To correct this error  
  
1.  If the `Continue` statement is in a `Do...Loop` loop, change the statement to `Continue Do`.  
  
2.  If the `Continue` statement is in a `For...Next` loop, change the statement to `Continue For`.  
  
3.  If the `Continue` statement is in a `While...End While` loop, change the statement to `Continue While`.  
  
4.  Otherwise, remove the `Continue` statement.  
  
## See Also  
 [Continue Statement (Visual Basic)](../vs140/Continue-Statement--Visual-Basic-.md)