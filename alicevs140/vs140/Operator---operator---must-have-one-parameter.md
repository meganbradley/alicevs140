---
title: "Operator &#39;&lt;operator&gt;&#39; must have one parameter"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 512a5724-a6c5-4437-a608-7d6b10e68d49
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Operator &#39;&lt;operator&gt;&#39; must have one parameter
A unary operator is defined with no parameters or with more than one parameter.  
  
 A unary operator must have exactly one parameter.  
  
 **Error ID:** BC33014  
  
### To correct this error  
  
-   Adjust the definition to specify exactly one parameter.  
  
-   If you need two parameters, you must define a binary operator.  
  
-   If you need no parameters or more than two, you must use the [Function Statement (Visual Basic)](../Topic/Function%20Statement%20\(Visual%20Basic\).md) to define a `Function` procedure instead of an operator.  
  
## See Also  
 [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md)   
 [Operator Statement](../vs140/Operator-Statement.md)   
 [How to: Define an Operator](../vs140/How-to--Define-an-Operator--Visual-Basic-.md)   
 [How to: Define a Conversion Operator](../vs140/How-to--Define-a-Conversion-Operator--Visual-Basic-.md)