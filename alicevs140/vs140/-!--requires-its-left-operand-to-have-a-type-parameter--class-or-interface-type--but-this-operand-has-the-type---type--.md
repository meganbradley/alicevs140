---
title: "&#39;!&#39; requires its left operand to have a type parameter, class or interface type, but this operand has the type &#39;&lt;type&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 95982e5e-c3e5-402e-ad7b-4c5076a13869
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;!&#39; requires its left operand to have a type parameter, class or interface type, but this operand has the type &#39;&lt;type&gt;&#39;
Dictionary member access, which uses an exclamation point (`!`) instead of a period (`.`), is valid only on a class or an interface.  
  
 **Error ID:** BC30103  
  
### To correct this error  
  
-   Replace the expression on the left of the exclamation point with one that evaluates to a defined class or interface type.  
  
## See Also  
 [Special Characters in Code](../vs140/Special-Characters-in-Code--Visual-Basic-.md)