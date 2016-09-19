---
title: "&#39;&lt;property1&gt;&#39; and &#39;&lt;property2&gt;&#39; cannot overload each other because only one is declared &#39;Default&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bac85b32-1a1f-4c43-817c-76e209cfeb8c
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;&lt;property1&gt;&#39; and &#39;&lt;property2&gt;&#39; cannot overload each other because only one is declared &#39;Default&#39;
If a property specifies `Default`, all properties overloaded on that name must also specify `Default`.  
  
 **Error ID:** BC30361  
  
### To correct this error  
  
-   Make sure all of the overloaded properties are declared `Default`.  
  
## See Also  
 [Considerations in Overloading Procedures](../vs140/Considerations-in-Overloading-Procedures--Visual-Basic-.md)   
 [Default](../vs140/Default--Visual-Basic-.md)