---
title: "Operators cannot be declared in Modules"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 10a8fd2d-2af7-4f90-9f2a-50c07ebf7589
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Operators cannot be declared in Modules
An [Operator Statement](../vs140/Operator-Statement.md) appears in a module definition.  
  
 You can define an operator as part of a class or a structure that you are defining. The operator must take that class or structure as at least one of its operands.  
  
 An operator must use an instance of a programming element as one of its operands, and only classes and structures have instances. Therefore, you cannot define an operator as part of any other programming element.  
  
 **Error ID:** BC33018  
  
### To correct this error  
  
-   If you require an operation on the module, use a [Function Statement (Visual Basic)](../Topic/Function%20Statement%20\(Visual%20Basic\).md) to define a `Function` procedure that performs the operation.  
  
-   You can also define a class or structure within the module and define an operator on that class or structure. However, that operator must take an instance of that class or structure as at least one of its operands.  
  
## See Also  
 [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md)   
 [How to: Define an Operator](../vs140/How-to--Define-an-Operator--Visual-Basic-.md)   
 [How to: Define a Conversion Operator](../vs140/How-to--Define-a-Conversion-Operator--Visual-Basic-.md)