---
title: "Boolean Operators (F#)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-fsharp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 65a2742d-7265-4681-8793-8e940b3adcf0
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Boolean Operators (F#)
This topic describes the support for Boolean operators in the F# language.  
  
## Summary of Boolean Operators  
 The following table summarizes the Boolean operators that are available in the F# language. The only type supported by these operators is the `bool` type.  
  
|Operator|Description|  
|--------------|-----------------|  
|`not`|Boolean negation|  
|`&#124;&#124;`|Boolean OR|  
|`&&`|Boolean AND|  
  
 The Boolean AND and OR operators perform *short-circuit evaluation*, that is, they evaluate the expression on the right of the operator only when it is necessary to determine the overall result of the expression. The second expression of the `&&` operator is evaluated only if the first expression evaluates to `true`; the second expression of the `||` operator is evaluated only if the first expression evaluates to `false`.  
  
## See Also  
 [Bitwise Operators](../vs140/Bitwise-Operators--F#-.md)   
 [Arithmetic Operators](../vs140/Arithmetic-Operators--F#-.md)   
 [Symbol and Operator Reference](../vs140/Symbol-and-Operator-Reference--F#-.md)