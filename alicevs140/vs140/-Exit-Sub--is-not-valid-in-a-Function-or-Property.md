---
title: "&#39;Exit Sub&#39; is not valid in a Function or Property"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d6426861-ba64-4dca-9100-262c6c058bd9
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Exit Sub&#39; is not valid in a Function or Property
`Exit Sub` appears in a `Function` procedure or a `Property` procedure. An `Exit` statement must match the block in which it occurs.  
  
 **Error ID:** BC30065  
  
### To correct this error  
  
-   Replace the `Exit Sub` with the `Exit Function` or `Exit Property` statement as appropriate.  
  
## See Also  
 [Sub Procedures](../vs140/Sub-Procedures--Visual-Basic-.md)   
 [Function Procedures](../Topic/Function%20Procedures%20\(Visual%20Basic\).md)   
 [Property Procedures](../vs140/Property-Procedures--Visual-Basic-.md)