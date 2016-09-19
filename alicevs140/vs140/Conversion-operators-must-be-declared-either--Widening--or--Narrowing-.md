---
title: "Conversion operators must be declared either &#39;Widening&#39; or &#39;Narrowing&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5972d955-ce1d-4348-a021-167eecb3a507
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Conversion operators must be declared either &#39;Widening&#39; or &#39;Narrowing&#39;
An [Operator Statement](../vs140/Operator-Statement.md) does not specify either [Widening](../vs140/Widening--Visual-Basic-.md) or [Narrowing](../vs140/Narrowing--Visual-Basic-.md).  
  
 When you define a conversion operator, you must declare it as either `Widening` or `Narrowing`. These are mutually exclusive characteristics, so you cannot specify both.  
  
 **Error ID:** BC33017  
  
### To correct this error  
  
-   Decide whether the conversion operator is to be `Widening` or `Narrowing`, and include the appropriate keyword in the `Operator` statement. You must specify one or the other.  
  
## See Also  
 [Widening and Narrowing Conversions](../Topic/Widening%20and%20Narrowing%20Conversions%20\(Visual%20Basic\).md)   
 [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md)   
 [Operator Statement](../vs140/Operator-Statement.md)   
 [How to: Define an Operator](../vs140/How-to--Define-an-Operator--Visual-Basic-.md)   
 [How to: Define a Conversion Operator](../vs140/How-to--Define-a-Conversion-Operator--Visual-Basic-.md)