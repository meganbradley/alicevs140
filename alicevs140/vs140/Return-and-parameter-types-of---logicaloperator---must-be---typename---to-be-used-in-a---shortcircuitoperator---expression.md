---
title: "Return and parameter types of &#39;&lt;logicaloperator&gt;&#39; must be &#39;&lt;typename&gt;&#39; to be used in a &#39;&lt;shortcircuitoperator&gt;&#39; expression"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 94cd52dc-5d48-4673-b0b8-38a1954483c6
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Return and parameter types of &#39;&lt;logicaloperator&gt;&#39; must be &#39;&lt;typename&gt;&#39; to be used in a &#39;&lt;shortcircuitoperator&gt;&#39; expression
An `And` operator or an `Or` operator is declared with unsuitable parameters or return type for use in an [AndAlso Operator](../vs140/AndAlso-Operator--Visual-Basic-.md) or an [OrElse Operator](../vs140/OrElse-Operator--Visual-Basic-.md).  
  
 Because you do not define a short-circuiting operator (`AndAlso` or `OrElse`) directly, you must define the corresponding logical and determinant operators. The following table shows the required operators.  
  
|Short-circuiting operator|Logical operator|Determinant operator|  
|--------------------------------|----------------------|--------------------------|  
|`AndAlso`|[And Operator](../vs140/And-Operator--Visual-Basic-.md)|[IsFalse Operator](../vs140/IsFalse-Operator--Visual-Basic-.md)|  
|`OrElse`|[Or Operator](../vs140/Or-Operator--Visual-Basic-.md)|[IsTrue Operator](../vs140/IsTrue-Operator--Visual-Basic-.md)|  
  
 [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] uses these logical and determinant operators to construct the short-circuiting logic for `AndAlso` or `OrElse`. For this to work properly, both operands and the return value of your `And` or `Or` definition must be of the containing type, that is, the type of the class or structure in which you are defining `And` or `Or`.  
  
 **Error ID:** BC33034  
  
### To correct this error  
  
-   Change the type of both operands and the return value to the type of the class or structure in which you are defining this operator.  
  
     -or-  
  
-   Do not use the corresponding short-circuiting operator (`AndAlso` or `OrElse`) with operands of the type of the class or structure in which you are defining this `And` or `Or` operator.  
  
## See Also  
 [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md)   
 [Operator Statement](../vs140/Operator-Statement.md)   
 [How to: Define an Operator](../vs140/How-to--Define-an-Operator--Visual-Basic-.md)   
 [How to: Define a Conversion Operator](../vs140/How-to--Define-a-Conversion-Operator--Visual-Basic-.md)   
 [Logical and Bitwise Operators in Visual Basic](../vs140/Logical-and-Bitwise-Operators-in-Visual-Basic.md)