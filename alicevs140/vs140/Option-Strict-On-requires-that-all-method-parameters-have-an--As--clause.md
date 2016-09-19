---
title: "Option Strict On requires that all method parameters have an &#39;As&#39; clause"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 855795ce-8499-4525-a1de-cbb8ba364cd7
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Option Strict On requires that all method parameters have an &#39;As&#39; clause
A method contains a parameter without an `As` clause. When `Option Strict` is on, every variable, property, procedure argument, and function return must be declared with an `As` clause to specify its data type; for example, `Sub GetData(ByVal filter As String)`.  
  
 **Error ID:** BC30211  
  
### To correct this error  
  
-   Check to see whether the `As` keyword is misspelled.  
  
-   Supply an `As` clause for the declared variable, or turn `Option Strict` off.  
  
## See Also  
 [Option Strict Statement](../vs140/Option-Strict-Statement.md)   
 [Sub Statement (Visual Basic)](../Topic/Sub%20Statement%20\(Visual%20Basic\).md)   
 [Function Statement (Visual Basic)](../Topic/Function%20Statement%20\(Visual%20Basic\).md)