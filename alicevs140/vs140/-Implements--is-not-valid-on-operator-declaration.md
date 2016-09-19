---
title: "&#39;Implements&#39; is not valid on operator declaration"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 22f27f4d-4bbd-4f8f-a6e8-0fc10efb268d
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Implements&#39; is not valid on operator declaration
An [Operator Statement](../vs140/Operator-Statement.md) specifies the [Implements (Visual Basic)](../vs140/Implements-Clause--Visual-Basic-.md) keyword.  
  
 Only a `Function` or `Sub` procedure, a property, or an event can implement an interface member. For more information on implementation, see [NOT IN BUILD: Interface Implementation Examples in Visual Basic](assetId:///50bf2a30-73b6-4126-a921-075fd6eec278).  
  
 An `Operator` procedure requires both the `Public` and `Shared` keywords, and a conversion operator requires either the `Widening` or the `Narrowing` keyword. For more information, see [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md).  
  
 **Error ID:** BC33004  
  
### To correct this error  
  
-   If you intend this procedure to implement an interface member, rewrite it as a `Function` or `Sub` procedure, a property, or an event.  
  
-   If you intend this procedure to define an operator, remove the `Implements` keyword from its declaration.  
  
## See Also  
 [Operator Statement](../vs140/Operator-Statement.md)   
 [How to: Define an Operator](../vs140/How-to--Define-an-Operator--Visual-Basic-.md)   
 [How to: Define a Conversion Operator](../vs140/How-to--Define-a-Conversion-Operator--Visual-Basic-.md)