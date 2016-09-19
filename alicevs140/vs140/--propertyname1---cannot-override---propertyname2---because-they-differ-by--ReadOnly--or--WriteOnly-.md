---
title: "&#39;&lt;propertyname1&gt;&#39; cannot override &#39;&lt;propertyname2&gt;&#39; because they differ by &#39;ReadOnly&#39; or &#39;WriteOnly&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 883deb25-e6db-403e-8c03-f580baf1afa9
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;&lt;propertyname1&gt;&#39; cannot override &#39;&lt;propertyname2&gt;&#39; because they differ by &#39;ReadOnly&#39; or &#39;WriteOnly&#39;
You have attempted to override a property with a second property that differs from the first only by `ReadOnly` or `WriteOnly`.  
  
 **Error ID:** BC30362  
  
### To correct this error  
  
-   Make sure the properties are differentiated by more than `ReadOnly` and `WriteOnly`.  
  
## See Also  
 [NOT IN BUILD: Overriding Properties and Methods](assetId:///2167e8f5-1225-4b13-9ebd-02591ba90213)   
 [Overrides](../vs140/Overrides--Visual-Basic-.md)