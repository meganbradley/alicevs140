---
title: "&#39;Return&#39; statement in a Sub or a Set cannot return a value"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d4c05c28-d650-4f49-976e-650d84802036
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Return&#39; statement in a Sub or a Set cannot return a value
`Sub` procedures and property `Set` procedures cannot return values.  
  
 **Error ID:** BC30647  
  
### To correct this error  
  
-   Change the current procedure to a function, or to a `Get` property procedure if the current procedure is part of a property.  
  
-   You can effectively return values from `Sub` procedures by modifying the value of parameters passed by reference using the `ByRef` keyword.  
  
## See Also  
 [Return Statement](../vs140/Return-Statement--Visual-Basic-.md)   
 [Sub Procedures](../vs140/Sub-Procedures--Visual-Basic-.md)   
 [Function Procedures](../Topic/Function%20Procedures%20\(Visual%20Basic\).md)   
 [Property Procedures](../vs140/Property-Procedures--Visual-Basic-.md)