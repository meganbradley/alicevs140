---
title: "&#39;&lt;declaration1&gt;&#39; cannot override &#39;&lt;declaration2&gt;&#39; because they have different access levels"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c9c5c14e-876c-430d-ab98-5087c19efae7
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;&lt;declaration1&gt;&#39; cannot override &#39;&lt;declaration2&gt;&#39; because they have different access levels
A procedure or property declaration attempts to override an inherited element of the same name, but it specifies a different accessibility than the inherited element. The inherited element's accessibility, such as `Public` or `Private`, must be preserved in overriding.  
  
 **Error ID:** BC30266  
  
### To correct this error  
  
-   Change the accessibility of the overriding element to match that of the inherited element.  
  
## See Also  
 [NOT IN BUILD: Overriding Properties and Methods](assetId:///2167e8f5-1225-4b13-9ebd-02591ba90213)   
 [Access Levels in Visual Basic](../vs140/Access-Levels-in-Visual-Basic.md)