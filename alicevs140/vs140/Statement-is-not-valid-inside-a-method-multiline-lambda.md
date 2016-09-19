---
title: "Statement is not valid inside a method-multiline lambda"
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
H1: Statement is not valid inside a method/multiline lambda
ms.assetid: 758e7a8f-429b-42c1-9a78-778e5b480e04
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Statement is not valid inside a method-multiline lambda
The statement is not valid within a `Sub`, `Function`, property `Get`, or property `Set` procedure. Some statements can be placed at the module or class level. Others, such as `Option Strict`, must be at namespace level and precede all other declarations.  
  
 **Error ID:** BC30024  
  
### To correct this error  
  
-   Remove the statement from the procedure.  
  
## See Also  
 [Sub Statement](../Topic/Sub%20Statement%20\(Visual%20Basic\).md)   
 [Function Statement](../Topic/Function%20Statement%20\(Visual%20Basic\).md)   
 [Get Statement](../vs140/Get-Statement.md)   
 [Set Statement](../vs140/Set-Statement--Visual-Basic-.md)