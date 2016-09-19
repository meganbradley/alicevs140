---
title: "Option Strict On requires all variable declarations to have an &#39;As&#39; clause"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 69c2e32a-86aa-4075-a142-440605a7063a
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Option Strict On requires all variable declarations to have an &#39;As&#39; clause
A declaration contains a declared variable without an `As` clause. When `Option Strict` is `On`, every variable, property, procedure argument, and function return must be declared with an `As` clause to specify its data type; for example, `Dim MyNum As Short`.  
  
 **Error ID:** BC30209  
  
### To correct this error  
  
1.  Check to see if the `As` keyword is misspelled.  
  
2.  Supply an `As` clause for the declared variable, or turn `Option Strict Off`.  
  
## See Also  
 [Option Strict Statement](../vs140/Option-Strict-Statement.md)   
 [Variable Declaration](../Topic/Variable%20Declaration%20in%20Visual%20Basic.md)