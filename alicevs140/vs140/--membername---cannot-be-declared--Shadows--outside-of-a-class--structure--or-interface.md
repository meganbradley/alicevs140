---
title: "&#39;&lt;membername&gt;&#39; cannot be declared &#39;Shadows&#39; outside of a class, structure, or interface"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 23e28894-5854-46ef-924d-f1cb6e81bcb1
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;&lt;membername&gt;&#39; cannot be declared &#39;Shadows&#39; outside of a class, structure, or interface
The `Shadows` keyword appears in a declaration at namespace, module, or file level. Shadowing is meaningful only within a programming element that can inherit from a base element.  
  
 **Error ID:** BC32200  
  
### To correct this error  
  
-   Remove the `Shadows` keyword, or move the declaration inside a class, structure, or interface.  
  
## See Also  
 [Shadows](../vs140/Shadows--Visual-Basic-.md)   
 [Shadowing in Visual Basic](../vs140/Shadowing-in-Visual-Basic.md)