---
title: "Only conversion operators can be declared &#39;&lt;keyword&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 946266fe-a909-41b1-aad4-f85dc8050b88
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Only conversion operators can be declared &#39;&lt;keyword&gt;&#39;
An [Operator Statement](../vs140/Operator-Statement.md) specifies [Widening](../vs140/Widening--Visual-Basic-.md) or [Narrowing](../vs140/Narrowing--Visual-Basic-.md) when the operator is not a conversion operator.  
  
 Every operator must be declared as both [Public (Visual Basic)](../vs140/Public--Visual-Basic-.md) and [Shared (Visual Basic)](../Topic/Shared%20\(Visual%20Basic\).md). However, only a conversion operator can be declared with [Widening](../vs140/Widening--Visual-Basic-.md) or [Narrowing](../vs140/Narrowing--Visual-Basic-.md), but not both.  
  
 An operator definition can optionally include the [Overloads](../vs140/Overloads--Visual-Basic-.md) and [Shadows](../vs140/Shadows--Visual-Basic-.md) keywords. No other keywords are permitted in an [Operator Statement](../vs140/Operator-Statement.md).  
  
 **Error ID:** BC33019  
  
### To correct this error  
  
1.  Remove the `Widening` or `Narrowing` keyword from the operator definition. These do not apply, because no type conversion is taking place.  
  
## See Also  
 [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md)   
 [Operator Statement](../vs140/Operator-Statement.md)   
 [How to: Define an Operator](../vs140/How-to--Define-an-Operator--Visual-Basic-.md)   
 [How to: Define a Conversion Operator](../vs140/How-to--Define-a-Conversion-Operator--Visual-Basic-.md)   
 [Type Conversions in Visual Basic](../vs140/Type-Conversions-in-Visual-Basic.md)