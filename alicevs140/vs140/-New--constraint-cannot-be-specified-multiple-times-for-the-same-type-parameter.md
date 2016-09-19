---
title: "&#39;New&#39; constraint cannot be specified multiple times for the same type parameter"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: afcb30da-3973-4452-9cf3-c027f9866589
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;New&#39; constraint cannot be specified multiple times for the same type parameter
A constraint list includes the [New (Visual Basic)](../vs140/New-Operator--Visual-Basic-.md) constraint more than once.  
  
 A constraint list on a type parameter can specify that the type argument passed to that type parameter must expose a parameterless constructor that the creating code can access. A type cannot have more than one parameterless constructor, and you cannot specify this requirement more than once.  
  
 **Error ID:** BC32081  
  
### To correct this error  
  
-   Remove any redundant `New` keywords. You should have only one in the constraint list.  
  
## See Also  
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)