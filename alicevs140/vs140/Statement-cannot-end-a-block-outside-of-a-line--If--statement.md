---
title: "Statement cannot end a block outside of a line &#39;If&#39; statement"
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
ms.assetid: 4039f51b-e0ee-4789-a89b-45d06de06b5d
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Statement cannot end a block outside of a line &#39;If&#39; statement
A single-line `If` statement contains several statements separated by colons (:), one of which is an `End` statement for a control block outside the single-line `If`. Single-line `If` statements do not use the `End If` statement.  
  
 **Error ID:** BC32005  
  
### To correct this error  
  
-   Move the single-line `If` statement outside the control block that contains the `End If` statement.  
  
## See Also  
 [If...Then...Else Statement](../Topic/If...Then...Else%20Statement%20\(Visual%20Basic\).md)