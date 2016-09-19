---
title: "Statements and labels are not valid between &#39;Select Case&#39; and first &#39;Case&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 399b4659-f7df-4377-80be-43019f1e6206
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Statements and labels are not valid between &#39;Select Case&#39; and first &#39;Case&#39;
A statement that is not a comment appears between the opening `Select` or `Select Case` statement and its first `Case` statement.  
  
 **Error ID:** BC30058  
  
### To correct this error  
  
-   If the intervening statement is a comment, precede it with a comment delimiter (`'` or `REM`). Otherwise, move or delete the statement.  
  
## See Also  
 [Select...Case Statement](../Topic/Select...Case%20Statement%20\(Visual%20Basic\).md)