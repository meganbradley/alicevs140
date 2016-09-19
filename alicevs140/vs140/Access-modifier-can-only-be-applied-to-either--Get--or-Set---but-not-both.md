---
title: "Access modifier can only be applied to either &#39;Get&#39; or Set&#39;, but not both"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c2a0580c-ff2f-4cc9-9113-6e540f906eec
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Access modifier can only be applied to either &#39;Get&#39; or Set&#39;, but not both
A property declaration specifies access levels in the [Property Statement](../vs140/Property-Statement.md), the [Get Statement](../vs140/Get-Statement.md), and the [Set Statement (Visual Basic)](../vs140/Set-Statement--Visual-Basic-.md).  
  
 You can always specify an access level for the property. In addition, you can specify a different access level for at most one of its property procedures (`Get` or `Set`), provided it is more restrictive than the property's access level. You cannot specify access levels for both of the property procedures.  
  
 **Error ID:** BC31101  
  
### To correct this error  
  
-   Remove the access modifier from either the `Get` statement or the `Set` statement.  
  
## See Also  
 [Property Procedures](../vs140/Property-Procedures--Visual-Basic-.md)   
 [How to: Declare a Property with Mixed Access Levels](../vs140/How-to--Declare-a-Property-with-Mixed-Access-Levels--Visual-Basic-.md)