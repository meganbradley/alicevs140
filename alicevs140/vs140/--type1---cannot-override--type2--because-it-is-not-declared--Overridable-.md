---
title: "&#39;&lt;type1&gt;&#39; cannot override &lt;type2&gt; because it is not declared &#39;Overridable&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ce071994-2e32-4460-a65d-f48f914386c6
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;&lt;type1&gt;&#39; cannot override &lt;type2&gt; because it is not declared &#39;Overridable&#39;
A member in a derived class overrides a base class member that is not marked with the `Overridable` modifier.  
  
 **Error ID:** BC31086  
  
### To correct this error  
  
1.  Add the `Overridable` modifier to the overridden member in the base class.  
  
2.  Use the `Shadows` keyword to shadow the item in the base class.  
  
## See Also  
 [Overridable](../vs140/Overridable--Visual-Basic-.md)   
 [Overrides](../vs140/Overrides--Visual-Basic-.md)   
 [Shadows](../vs140/Shadows--Visual-Basic-.md)