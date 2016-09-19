---
title: "&#39;Sub New&#39; cannot handle events"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b8a546c4-914e-49de-b553-9fc0f41424ed
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Sub New&#39; cannot handle events
You attempted to combine `Sub New` with `Handles`, which is invalid. Use the `Handles` keyword at the end of a procedure declaration to cause it to handle events raised by an object variable declared using the `WithEvents` keyword.  
  
 **Error ID:** BC30497  
  
### To correct this error  
  
1.  Do not use `New` in this context.  
  
## See Also  
 [Handles](../vs140/Handles-Clause--Visual-Basic-.md)   
 [Dim Statement](../Topic/Dim%20Statement%20\(Visual%20Basic\).md)   
 [WithEvents](../vs140/WithEvents--Visual-Basic-.md)