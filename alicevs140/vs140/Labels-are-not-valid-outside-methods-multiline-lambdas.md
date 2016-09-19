---
title: "Labels are not valid outside methods-multiline lambdas"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
H1: Labels are not valid outside methods/multiline lambdas
ms.assetid: 17d12a96-d759-4df9-882c-5e45c1d814a5
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Labels are not valid outside methods-multiline lambdas
You can add a label to a statement only within a `Sub`, `Function`, property `Get`, or property `Set` procedure. Only an executable statement can have a label, and all executable statements must be inside procedures.  
  
 **Error ID:** BC30016  
  
### To correct this error  
  
1.  Remove the label from the statement, or move the statement inside a procedure.  
  
## See Also  
 [How to: Label Statements](../vs140/How-to--Label-Statements--Visual-Basic-.md)   
 [Sub Statement](../Topic/Sub%20Statement%20\(Visual%20Basic\).md)   
 [Function Statement](../Topic/Function%20Statement%20\(Visual%20Basic\).md)   
 [Get Statement](../vs140/Get-Statement.md)   
 [Set Statement](../vs140/Set-Statement--Visual-Basic-.md)