---
title: "Operators cannot be declared &#39;&lt;keyword&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bfd805f4-e30e-4553-9cb7-2690595f0480
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Operators cannot be declared &#39;&lt;keyword&gt;&#39;
An operator is declared with a keyword that is not valid for operator definitions.  
  
 Every operator must be declared as both [Public (Visual Basic)](../vs140/Public--Visual-Basic-.md) and [Shared (Visual Basic)](../Topic/Shared%20\(Visual%20Basic\).md). In addition, a conversion operator must be declared with either [Widening](../vs140/Widening--Visual-Basic-.md) or [Narrowing](../vs140/Narrowing--Visual-Basic-.md), but not both. An operator definition can optionally include the [Overloads](../vs140/Overloads--Visual-Basic-.md) or [Shadows](../vs140/Shadows--Visual-Basic-.md) keywords. No other keywords are permitted in an [Operator Statement](../vs140/Operator-Statement.md).  
  
 **Error ID:** BC33013  
  
### To correct this error  
  
-   Remove the invalid keyword from the operator definition.  
  
## See Also  
 [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md)   
 [How to: Define an Operator](../vs140/How-to--Define-an-Operator--Visual-Basic-.md)   
 [How to: Define a Conversion Operator](../vs140/How-to--Define-a-Conversion-Operator--Visual-Basic-.md)