---
title: "&#39;Widening&#39; and &#39;Narrowing&#39; cannot be combined"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1c576344-083c-45ad-bc71-0489bd3976be
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Widening&#39; and &#39;Narrowing&#39; cannot be combined
An [Operator Statement](../vs140/Operator-Statement.md) specifies both [Widening](../vs140/Widening--Visual-Basic-.md) and [Narrowing](../vs140/Narrowing--Visual-Basic-.md).  
  
 When you define a conversion operator, you must declare it as either `Widening` or `Narrowing`. These are mutually exclusive characteristics, so you cannot specify both.  
  
 **Error ID:** BC33001  
  
### To correct this error  
  
-   Remove either the `Widening` or the `Narrowing` keyword from the `Operator` statement. You must specify one or the other.  
  
## See Also  
 [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md)   
 [Operator Statement](../vs140/Operator-Statement.md)   
 [How to: Define an Operator](../vs140/How-to--Define-an-Operator--Visual-Basic-.md)   
 [How to: Define a Conversion Operator](../vs140/How-to--Define-a-Conversion-Operator--Visual-Basic-.md)