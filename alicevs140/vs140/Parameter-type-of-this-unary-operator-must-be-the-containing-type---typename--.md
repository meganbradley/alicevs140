---
title: "Parameter type of this unary operator must be the containing type &#39;&lt;typename&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9c2c2c5b-6f18-49d2-bd6e-e735a6bced77
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Parameter type of this unary operator must be the containing type &#39;&lt;typename&gt;&#39;
A definition of a unary operator specifies a parameter with a type other than that of the class or structure in which the operator is defined.  
  
 When you define an operator in a class or structure, at least one of the parameters must be of the type of that class or structure. In the case of a unary operator, the sole operand must be of the type of that class or structure.  
  
 **Error ID:** BC33020  
  
### To correct this error  
  
-   Change the parameter type to the type of the class or structure in which the operator is defined.  
  
-   If you want to take one data type as a parameter and return a different data type as the result of the operation, define a conversion operator instead.  
  
## See Also  
 [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md)   
 [Operator Statement](../vs140/Operator-Statement.md)   
 [How to: Define an Operator](../vs140/How-to--Define-an-Operator--Visual-Basic-.md)   
 [How to: Define a Conversion Operator](../vs140/How-to--Define-a-Conversion-Operator--Visual-Basic-.md)