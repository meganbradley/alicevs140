---
title: "&#39;ReadOnly&#39; properties cannot have an access modifier on &#39;Get&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 54066d8e-eb22-4b99-bb18-45afe61d3b33
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;ReadOnly&#39; properties cannot have an access modifier on &#39;Get&#39;
A `ReadOnly` property declaration specifies access levels in both the [Property Statement](../vs140/Property-Statement.md) and the [Get Statement](../vs140/Get-Statement.md).  
  
 You can always specify an access level for the property. In addition, you can specify a different access level for at most one of its property procedures (`Get` or `Set`), provided it is more restrictive than the property's access level. You cannot specify access levels for both of the property procedures.  
  
 **Error ID:** BC31105  
  
### To correct this error  
  
-   Remove the access modifier from the `Get` statement. It represents the entire `ReadOnly` property, and you cannot have two access levels for the property.  
  
## See Also  
 [Property Procedures](../vs140/Property-Procedures--Visual-Basic-.md)   
 [How to: Declare a Property with Mixed Access Levels](../vs140/How-to--Declare-a-Property-with-Mixed-Access-Levels--Visual-Basic-.md)