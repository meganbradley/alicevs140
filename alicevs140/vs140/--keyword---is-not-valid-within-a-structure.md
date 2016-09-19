---
title: "&#39;&lt;keyword&gt;&#39; is not valid within a structure"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 252510cf-e084-47e4-9592-4aa8f94fabe4
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;&lt;keyword&gt;&#39; is not valid within a structure
Structures are value types, not reference types. A structure is not an instance created from a class, so the `Me`, `MyClass`, and `MyBase` keywords are meaningless in a structure.  
  
 **Error ID:** BC30044  
  
### To correct this error  
  
-   Change the structure to a class, or remove the keyword from the procedure.  
  
## See Also  
 [Me](assetId:///a65973c7-cf06-4547-9b25-9fba885525c2)   
 [MyClass - delete](assetId:///5db36f9b-f796-4b6a-ba34-cac1fde6eb62)   
 [MyBase - delete](assetId:///52491d06-6451-4f6f-9aa6-8fab59bbc2b9)   
 [Inheritance Basics](../vs140/Inheritance-Basics--Visual-Basic-.md)