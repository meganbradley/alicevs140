---
title: "Property cannot be declared &#39;&lt;propertymodifier&gt;&#39; because it contains a &#39;Private&#39; accessor"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 74fb36f4-54cd-4fda-bcc6-e965b5c7c37b
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Property cannot be declared &#39;&lt;propertymodifier&gt;&#39; because it contains a &#39;Private&#39; accessor
A property with a `Private` property procedure (`Get` or `Set`) is marked [Overridable](../vs140/Overridable--Visual-Basic-.md).  
  
 If a base class property or procedure is declared [Private (Visual Basic)](../vs140/Private--Visual-Basic-.md), a derived class cannot override that property or procedure because it cannot access it. Because of this, you cannot use `Private` in combination with `Overridable`. This applies not only to the property itself but to the individual property procedures as well.  
  
 **Error ID:** BC31108  
  
### To correct this error  
  
-   Remove the `Overridable` keyword from the [Property Statement](../vs140/Property-Statement.md), or remove the `Private` keyword from the [Get Statement](../vs140/Get-Statement.md) or the [Set Statement (Visual Basic)](../vs140/Set-Statement--Visual-Basic-.md).  
  
## See Also  
 [Property Procedures](../vs140/Property-Procedures--Visual-Basic-.md)   
 [How to: Declare a Property with Mixed Access Levels](../vs140/How-to--Declare-a-Property-with-Mixed-Access-Levels--Visual-Basic-.md)