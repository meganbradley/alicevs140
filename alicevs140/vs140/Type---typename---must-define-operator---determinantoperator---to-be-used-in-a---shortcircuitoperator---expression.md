---
title: "Type &#39;&lt;typename&gt;&#39; must define operator &#39;&lt;determinantoperator&gt;&#39; to be used in a &#39;&lt;shortcircuitoperator&gt;&#39; expression"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 50a0a39f-63cd-4100-aea9-91b5b6ab5bbf
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Type &#39;&lt;typename&gt;&#39; must define operator &#39;&lt;determinantoperator&gt;&#39; to be used in a &#39;&lt;shortcircuitoperator&gt;&#39; expression
An [AndAlso Operator](../vs140/AndAlso-Operator--Visual-Basic-.md) or an [OrElse Operator](../vs140/OrElse-Operator--Visual-Basic-.md) uses operands of a class or structure type, when that class or structure does not define a required operator.  
  
 Because you do not define a short-circuiting operator (`AndAlso` or `OrElse`) directly, you must define the corresponding logical and determinant operators. The following table shows the required operators.  
  
|Short-circuiting operator|Logical operator|Determinant operator|  
|--------------------------------|----------------------|--------------------------|  
|`AndAlso`|[And Operator](../vs140/And-Operator--Visual-Basic-.md)|[IsFalse Operator](../vs140/IsFalse-Operator--Visual-Basic-.md)|  
|`OrElse`|[Or Operator](../vs140/Or-Operator--Visual-Basic-.md)|[IsTrue Operator](../vs140/IsTrue-Operator--Visual-Basic-.md)|  
  
 [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] uses these logical and determinant operators to construct the short-circuiting logic for `AndAlso` or `OrElse`. For this to work properly, both operands and the return value of your `And` or `Or` definition must be of the containing type, that is, the type of the class or structure in which you are defining `And` or `Or`.  
  
 **Error ID:** BC33035  
  
### To correct this error  
  
-   Define the `And` and `IsFalse` operators, or the `Or` and `IsTrue` operators, in the class or structure used for the operand type of the `AndAlso` or `OrElse` operator. Be sure the operands for `And` or `Or` are of the type of the class or structure in which you define it.  
  
## See Also  
 [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md)   
 [Operator Statement](../vs140/Operator-Statement.md)   
 [How to: Define an Operator](../vs140/How-to--Define-an-Operator--Visual-Basic-.md)   
 [How to: Define a Conversion Operator](../vs140/How-to--Define-a-Conversion-Operator--Visual-Basic-.md)   
 [Logical and Bitwise Operators in Visual Basic](../vs140/Logical-and-Bitwise-Operators-in-Visual-Basic.md)