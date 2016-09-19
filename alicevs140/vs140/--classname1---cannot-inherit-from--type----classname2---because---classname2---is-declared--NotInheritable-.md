---
title: "&#39;&lt;classname1&gt;&#39; cannot inherit from &lt;type&gt; &#39;&lt;classname2&gt;&#39; because &#39;&lt;classname2&gt;&#39; is declared &#39;NotInheritable&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 627d50f5-9e75-495d-93f7-50096ba2ea08
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;&lt;classname1&gt;&#39; cannot inherit from &lt;type&gt; &#39;&lt;classname2&gt;&#39; because &#39;&lt;classname2&gt;&#39; is declared &#39;NotInheritable&#39;
A class attempts to inherit from another class, but the desired base class is specified as `NotInheritable`. `NotInheritable` classes are used primarily to prevent unintended derivation.  
  
 **Error ID:** BC30299  
  
### To correct this error  
  
-   Remove the `NotInheritable` keyword from the definition of the desired base class, or remove the `Inherits` statement.  
  
## See Also  
 [Inheritance Basics](../vs140/Inheritance-Basics--Visual-Basic-.md)   
 [NotInheritable](../vs140/NotInheritable--Visual-Basic-.md)   
 [Inherits Statement](../vs140/Inherits-Statement.md)