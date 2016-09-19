---
title: "Variable declaration without an &#39;As&#39; clause; type of Object assumed"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9422b16d-39b5-4d49-b697-608226ccafea
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Variable declaration without an &#39;As&#39; clause; type of Object assumed
A variable declaration does not specify an `As` clause.  
  
 An `As` clause identifies a data type to be associated with a programming element. In a [Dim Statement (Visual Basic)](../Topic/Dim%20Statement%20\(Visual%20Basic\).md), it specifies the data type of the variable or variables. If you do not include an `As` clause in the `Dim` statement, the variable's data type defaults to `Object`.  
  
 By default, this message is a warning. For information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../vs140/Configuring-Warnings-in-Visual-Basic.md).  
  
 **Error ID:** BC42020  
  
### To correct this error  
  
-   Include an `As` clause in the `Dim` statement to specify the variable's data type.  
  
## See Also  
 [Dim Statement (Visual Basic)](../Topic/Dim%20Statement%20\(Visual%20Basic\).md)   
 [Variable Declaration in Visual Basic](../Topic/Variable%20Declaration%20in%20Visual%20Basic.md)