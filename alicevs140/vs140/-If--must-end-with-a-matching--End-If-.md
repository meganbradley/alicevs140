---
title: "&#39;If&#39; must end with a matching &#39;End If&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e5905d59-56bb-4daf-aca5-5ff847fc62f6
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;If&#39; must end with a matching &#39;End If&#39;
An `If` statement occurs without a corresponding `End If` statement. An `End If` statement must be used to end the `If` block.  
  
 **Error ID:** BC30081  
  
### To correct this error  
  
1.  If this `If` block is part of a set of nested `If` blocks, make sure each block is properly terminated.  
  
2.  Add an `End If` statement to the end of the `If` block.  
  
## See Also  
 [If...Then...Else Statement](../Topic/If...Then...Else%20Statement%20\(Visual%20Basic\).md)