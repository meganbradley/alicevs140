---
title: "Leading &#39;.&#39; or &#39;!&#39; can only appear inside a &#39;With&#39; statement"
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
ms.assetid: 70daaee1-14f9-45b7-9f30-53794310b95e
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Leading &#39;.&#39; or &#39;!&#39; can only appear inside a &#39;With&#39; statement
A period (.) or exclamation point (!) that is not inside a `With` block occurs without an expression on the left. Member access (`.`) and dictionary member access (`!`) require an expression specifying the element that contains the member. This must appear immediately to the left of the accessor or as the target of a `With` block containing the member access.  
  
 **Error ID:** BC30157  
  
### To correct this error  
  
1.  Ensure that the `With` block is correctly formatted.  
  
2.  If there is no `With` block, add an expression to the left of the accessor that evaluates to a defined element containing the member.  
  
## See Also  
 [Special Characters in Code](../vs140/Special-Characters-in-Code--Visual-Basic-.md)   
 [With...End With Statement](../Topic/With...End%20With%20Statement%20\(Visual%20Basic\).md)