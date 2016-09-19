---
title: "Operators must be declared &#39;Shared&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5ad97616-4032-46cd-aaf7-517db5d1195f
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Operators must be declared &#39;Shared&#39;
An [Operator Statement](../vs140/Operator-Statement.md) does not include the [Shared (Visual Basic)](../Topic/Shared%20\(Visual%20Basic\).md) keyword.  
  
 An `Operator` procedure requires both the [Public (Visual Basic)](../vs140/Public--Visual-Basic-.md) and `Shared` keywords, and a conversion operator also requires either the [Widening](../vs140/Widening--Visual-Basic-.md) or the [Narrowing](../vs140/Narrowing--Visual-Basic-.md) keyword.  
  
 **Error ID:** BC33012  
  
### To correct this error  
  
-   Add the `Shared` keyword to the `Operator` statement.  
  
## See Also  
 [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md)   
 [Operator Statement](../vs140/Operator-Statement.md)   
 [How to: Define an Operator](../vs140/How-to--Define-an-Operator--Visual-Basic-.md)   
 [How to: Define a Conversion Operator](../vs140/How-to--Define-a-Conversion-Operator--Visual-Basic-.md)