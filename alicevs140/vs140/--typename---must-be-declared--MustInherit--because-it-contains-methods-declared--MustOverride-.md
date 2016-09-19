---
title: "&#39;&lt;typename&gt;&#39; must be declared &#39;MustInherit&#39; because it contains methods declared &#39;MustOverride&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5a9f4c57-a4b8-45f5-8273-b7caa689a170
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;&lt;typename&gt;&#39; must be declared &#39;MustInherit&#39; because it contains methods declared &#39;MustOverride&#39;
Types that contain `MustOverride` members must be declared `MustInherit`.  
  
 **Error ID:** BC31411  
  
### To correct this error  
  
-   Add the `MustInherit` modifier to the type.  
  
## See Also  
 [MustInherit](../Topic/MustInherit%20\(Visual%20Basic\).md)   
 [MustOverride](../vs140/MustOverride--Visual-Basic-.md)