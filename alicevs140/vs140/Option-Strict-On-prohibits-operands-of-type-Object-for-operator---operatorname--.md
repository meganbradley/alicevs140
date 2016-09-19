---
title: "Option Strict On prohibits operands of type Object for operator &#39;&lt;operatorname&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: eb047d36-1fb4-460d-ae98-c76f31a89bed
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Option Strict On prohibits operands of type Object for operator &#39;&lt;operatorname&gt;&#39;
The only operators defined for object variables are `Is` and `TypeOf...Is`. When `Option Strict` is `On`, all operands must be of data types defined for the given operator.  
  
 **Error ID:** BC30038  
  
### To correct this error  
  
-   Use the appropriate type conversion functions, such as `CInt` or `CStr`, to convert the operands to data types defined for the operator.  
  
## See Also  
 [Is Operator](../vs140/Is-Operator--Visual-Basic-.md)   
 [Comparison Operators in Visual Basic](../vs140/Comparison-Operators-in-Visual-Basic.md)   
 [Type Conversion Functions](../vs140/Type-Conversion-Functions--Visual-Basic-.md)