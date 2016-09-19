---
title: "&#39;WriteOnly&#39; properties cannot have an access modifier on &#39;Set&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d1ac04a8-e436-4f3e-8d71-fc4569b35fcd
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;WriteOnly&#39; properties cannot have an access modifier on &#39;Set&#39;
A `WriteOnly` property declaration specifies access levels in both the [Property Statement](../vs140/Property-Statement.md) and the [Set Statement (Visual Basic)](../vs140/Set-Statement--Visual-Basic-.md).  
  
 You can always specify an access level for the property. In addition, you can specify a different access level for at most one of its property procedures (`Get` or `Set`), provided it is more restrictive than the property's access level. You cannot specify access levels for both of the property procedures.  
  
 **Error ID:** BC31104  
  
### To correct this error  
  
-   Remove the access modifier from the `Set` statement. It represents the entire `WriteOnly` property, and you cannot have two access levels for the property.  
  
## See Also  
 [Property Procedures](../vs140/Property-Procedures--Visual-Basic-.md)   
 [How to: Declare a Property with Mixed Access Levels](../vs140/How-to--Declare-a-Property-with-Mixed-Access-Levels--Visual-Basic-.md)