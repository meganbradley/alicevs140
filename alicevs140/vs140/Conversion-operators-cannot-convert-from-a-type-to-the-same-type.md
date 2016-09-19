---
title: "Conversion operators cannot convert from a type to the same type"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4b47bcb0-4f0c-4d1c-9274-cce5b8e2b370
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Conversion operators cannot convert from a type to the same type
A conversion operator is declared with the same type for both the parameter and the return.  
  
 It is not meaningful to convert from any type to itself.  
  
 **Error ID:** BC33024  
  
### To correct this error  
  
-   Change the type of either the parameter or the return value. One of them must be of the type of the class or structure in which this operator is defined. The other must be of a different type.  
  
-   If you need to perform a transformation on the contents of the parameter, use a [Function Statement (Visual Basic)](../Topic/Function%20Statement%20\(Visual%20Basic\).md) to define a `Function` procedure instead of an operator.  
  
## See Also  
 [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md)   
 [Operator Statement](../vs140/Operator-Statement.md)   
 [How to: Define an Operator](../vs140/How-to--Define-an-Operator--Visual-Basic-.md)   
 [How to: Define a Conversion Operator](../vs140/How-to--Define-a-Conversion-Operator--Visual-Basic-.md)