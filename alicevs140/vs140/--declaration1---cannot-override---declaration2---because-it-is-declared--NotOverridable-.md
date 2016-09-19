---
title: "&#39;&lt;declaration1&gt;&#39; cannot override &#39;&lt;declaration2&gt;&#39; because it is declared &#39;NotOverridable&#39;"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fb1f6797-4e49-442e-a660-59d602132631
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;&lt;declaration1&gt;&#39; cannot override &#39;&lt;declaration2&gt;&#39; because it is declared &#39;NotOverridable&#39;
A procedure or property declaration attempts to override an inherited element of the same name, but the inherited element is specified as `NotOverridable`.  
  
 **Error ID:** BC30267  
  
### To correct this error  
  
-   Remove the `NotOverridable` keyword from the declaration of the inherited element, or remove the overriding declaration.  
  
## See Also  
 [NOT IN BUILD: Overriding Properties and Methods](assetId:///2167e8f5-1225-4b13-9ebd-02591ba90213)