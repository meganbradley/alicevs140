---
title: "&#39;End With&#39; must be preceded by a matching &#39;With&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b0f1f7d5-0c33-4b97-8043-f0f5b40ca5d7
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;End With&#39; must be preceded by a matching &#39;With&#39;
An `End With` statement occurs without a corresponding `With` statement. `End With` must be preceded by a corresponding `With` statement.  
  
 **Error ID:** BC30093  
  
### To correct this error  
  
1.  If this `With` block is part of a set of nested `With` blocks, make sure each block is properly terminated.  
  
2.  Verify that other control structures within the `With` block are correctly terminated.  
  
3.  Ensure that this `With` block is correctly formatted.  
  
## See Also  
 [With...End With Statement](../Topic/With...End%20With%20Statement%20\(Visual%20Basic\).md)