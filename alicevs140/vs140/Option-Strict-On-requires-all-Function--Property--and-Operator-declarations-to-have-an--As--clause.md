---
title: "Option Strict On requires all Function, Property, and Operator declarations to have an &#39;As&#39; clause"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4d217e56-0eac-4834-bcad-234a69809390
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Option Strict On requires all Function, Property, and Operator declarations to have an &#39;As&#39; clause
A declaration contains a declared property or function return without an `As` clause. When `Option Strict` is `On`, every variable, property, procedure argument, and function return must be declared with an `As` clause to specify its data type; for example, `Dim MyNum As Short`.  
  
 **Error ID:** BC30210  
  
### To correct this error  
  
1.  Check to see if the `As` keyword is misspelled.  
  
2.  Supply an `As` clause for the declared property or function return, or turn `Option Strict Off`.  
  
## See Also  
 [Option Strict Statement](../vs140/Option-Strict-Statement.md)   
 [Property Procedures](../vs140/Property-Procedures--Visual-Basic-.md)   
 [Function Procedures](../Topic/Function%20Procedures%20\(Visual%20Basic\).md)