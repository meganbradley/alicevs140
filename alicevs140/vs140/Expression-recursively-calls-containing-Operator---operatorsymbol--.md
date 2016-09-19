---
title: "Expression recursively calls containing Operator &#39;&lt;operatorsymbol&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a874c44a-3aec-447d-90f7-5659f1b2f5f6
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Expression recursively calls containing Operator &#39;&lt;operatorsymbol&gt;&#39;
An expression within an operator procedure uses the operator being defined. This results in the operator procedure calling itself because of the data types being used.  
  
 The operator procedure you are defining calls itself if it uses the same operator with any of the following:  
  
-   The same operands for which you are defining the operator;  
  
-   Operands of the same data types for which you are defining the operator; or  
  
-   Operands of data types that widen to the data types for which you are defining the operator.  
  
 A *recursive call* is when a procedure calls itself. Recursive calls can result in an *infinite loop*, in which control passes through the same set of statements repeatedly until your application is terminated externally. If your code does not include one or more tests that can be used to terminate recursion, you risk an infinite loop.  
  
 By default, this message is a warning. For information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../vs140/Configuring-Warnings-in-Visual-Basic.md).  
  
 **Error ID:** BC42004  
  
### To correct this error  
  
-   If your logic requires the operator procedure to call itself, then be sure you test for at least one condition that is certain to occur at some point, and use this test to terminate the recursive calls.  
  
-   If your logic does not require the operator procedure to call itself, then remove any recursive calls or replace them with statements that do not call their own procedure.  
  
## See Also  
 [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md)   
 [Operator Statement](../vs140/Operator-Statement.md)   
 [How to: Define an Operator](../vs140/How-to--Define-an-Operator--Visual-Basic-.md)   
 [How to: Define a Conversion Operator](../vs140/How-to--Define-a-Conversion-Operator--Visual-Basic-.md)