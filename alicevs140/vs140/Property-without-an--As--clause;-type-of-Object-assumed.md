---
title: "Property without an &#39;As&#39; clause; type of Object assumed"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3379692b-8278-4488-878a-0afb76e554b1
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Property without an &#39;As&#39; clause; type of Object assumed
A property declaration does not specify an `As` clause.  
  
 An `As` clause identifies a data type to be associated with a programming element. In a [Property Statement](../vs140/Property-Statement.md), it specifies the data type of the value that the property's `Get` procedure returns to the calling code. If you do not include an `As` clause in the `Property` statement, the property's data type defaults to `Object`.  
  
 By default, this message is a warning. For more information about hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../vs140/Configuring-Warnings-in-Visual-Basic.md).  
  
 **Error ID:** BC42022  
  
### To correct this error  
  
-   Include an `As` clause in the `Property` statement to specify the property's data type.  
  
## See Also  
 [Property Procedures](../vs140/Property-Procedures--Visual-Basic-.md)   
 [Property Statement](../vs140/Property-Statement.md)   
 [Get Statement](../vs140/Get-Statement.md)