---
title: "&#39;Exit While&#39; can only appear inside a &#39;While&#39; statement"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cf0a3e09-5252-4198-bb27-c103c98d9f19
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Exit While&#39; can only appear inside a &#39;While&#39; statement
An `Exit While` statement occurs outside a `While` block. `Exit While` is valid only between a `While` statement and a corresponding `End While` statement.  
  
 **Error ID:** BC30097  
  
### To correct this error  
  
1.  Make sure a valid `While` statement precedes the `Exit While` and a valid `End While` statement appears after it.  
  
2.  Verify that other control structures within the `While` block are correctly terminated.  
  
## See Also  
 [While...End While Statement](../Topic/While...End%20While%20Statement%20\(Visual%20Basic\).md)