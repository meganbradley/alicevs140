---
title: "Operator without an &#39;As&#39; clause; type of Object assumed"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 42be84ed-7aa6-4ac0-9dd4-663e90f13e09
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Operator without an &#39;As&#39; clause; type of Object assumed
An operator procedure does not specify an `As` clause.  
  
 An `As` clause identifies a data type to be associated with a programming element. In an [Operator Statement](../vs140/Operator-Statement.md), it specifies the data type of the value the operator procedure returns to the calling code. If you do not include an `As` clause in the `Operator` statement, the return data type defaults to `Object`.  
  
 By default, this message is a warning. For information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../vs140/Configuring-Warnings-in-Visual-Basic.md).  
  
 **Error ID:** BC41005  
  
### To correct this error  
  
-   Include an `As` clause in the `Operator` statement to specify the return data type.  
  
## See Also  
 [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md)   
 [Operator Statement](../vs140/Operator-Statement.md)