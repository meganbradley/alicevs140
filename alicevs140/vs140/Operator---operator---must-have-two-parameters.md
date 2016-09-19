---
title: "Operator &#39;&lt;operator&gt;&#39; must have two parameters"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 506ea996-8abe-4dbe-aff4-d3910bf4399e
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Operator &#39;&lt;operator&gt;&#39; must have two parameters
A binary operator is defined with fewer than two or more than two parameters.  
  
 A binary operator must have exactly two parameters.  
  
 **Error ID:** BC33015  
  
### To correct this error  
  
-   Adjust the definition to specify exactly two parameters.  
  
-   If you need only one parameter, you must define a unary operator.  
  
-   If you need no parameters or more than two, you must use the [Function Statement (Visual Basic)](../Topic/Function%20Statement%20\(Visual%20Basic\).md) to define a `Function` procedure instead of an operator.  
  
## See Also  
 [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md)   
 [Operator Statement](../vs140/Operator-Statement.md)   
 [How to: Define an Operator](../vs140/How-to--Define-an-Operator--Visual-Basic-.md)   
 [How to: Define a Conversion Operator](../vs140/How-to--Define-a-Conversion-Operator--Visual-Basic-.md)