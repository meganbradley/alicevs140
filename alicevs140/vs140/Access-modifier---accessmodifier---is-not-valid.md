---
title: "Access modifier &#39;&lt;accessmodifier&gt;&#39; is not valid"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1cd71acc-0b54-4f64-8d61-75b272d293cb
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Access modifier &#39;&lt;accessmodifier&gt;&#39; is not valid
A [Get Statement](../vs140/Get-Statement.md) or [Set Statement (Visual Basic)](../vs140/Set-Statement--Visual-Basic-.md) specifies an access level that is less restrictive than that specified for the containing property.  
  
 You can always specify an access level for the property. In addition, you can specify a different access level for at most one of its property procedures (`Get` or `Set`), provided it is more restrictive than the property's access level. For example, if the property is `Friend`, you can specify `Private` for a property procedure, but not `Public`. You cannot specify access levels for both of the property procedures.  
  
 **Error ID:** BC31100  
  
### To correct this error  
  
-   Make the access level for the property procedure more restrictive than for the property, or remove the access modifier entirely.  
  
-   Declare the less restrictive access level in the [Property Statement](../vs140/Property-Statement.md), and declare the more restrictive access level in one of the property procedures.  
  
## See Also  
 [Property Procedures](../vs140/Property-Procedures--Visual-Basic-.md)   
 [How to: Declare a Property with Mixed Access Levels](../vs140/How-to--Declare-a-Property-with-Mixed-Access-Levels--Visual-Basic-.md)