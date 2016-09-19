---
title: "&#39;&lt;keyword&gt;&#39; is valid only within a class"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 773d8d50-abb8-4257-83a5-6e017c199d82
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;&lt;keyword&gt;&#39; is valid only within a class
A keyword related to classes, such as `Me` or `MyClass`, is used outside of a class definition.  
  
 **Error ID:** BC32002  
  
### To correct this error  
  
-   If the code using the keyword involves class instances, move it to a class implementation.  
  
-   If the code using the keyword does not apply to classes, remove the invalid keyword.  
  
## See Also  
 [Me](assetId:///a65973c7-cf06-4547-9b25-9fba885525c2)   
 [MyClass - delete](assetId:///5db36f9b-f796-4b6a-ba34-cac1fde6eb62)   
 [Class Statement](../Topic/Class%20Statement%20\(Visual%20Basic\).md)