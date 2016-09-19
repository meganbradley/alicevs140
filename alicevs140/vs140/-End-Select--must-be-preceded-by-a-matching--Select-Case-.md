---
title: "&#39;End Select&#39; must be preceded by a matching &#39;Select Case&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9de8c0d4-4ce9-45cf-98d6-8f68bba507a5
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;End Select&#39; must be preceded by a matching &#39;Select Case&#39;
An `End Select` statement occurs without a corresponding `Select` or `Select Case` statement. `End Select` must be preceded by a `Select` or `Select Case` statement.  
  
 **Error ID:** BC30088  
  
### To correct this error  
  
1.  If this `Select` block is part of a set of nested `Select` blocks, make sure each block is properly terminated.  
  
2.  Verify that other control structures within the `Select` block are correctly terminated.  
  
3.  Check that this `Select` block is correctly formatted.  
  
## See Also  
 [Select...Case Statement](../Topic/Select...Case%20Statement%20\(Visual%20Basic\).md)