---
title: "&#39;New&#39; cannot be used on a class that is declared &#39;MustInherit&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 94c9e6a3-6489-4d58-b7e5-7b4203677e3b
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;New&#39; cannot be used on a class that is declared &#39;MustInherit&#39;
A `MustInherit` class cannot be instantiated directly, and therefore the `New` operator cannot be used on a `MustInherit` class. Although it's possible to have variables and values whose compile time types are `MustInherit`, such variables and values will necessarily either be a null value or contain references to instances of regular classes derived from the `MustInherit` types.  
  
 **Error ID:** BC30569  
  
### To correct this error  
  
-   Remove the `New` operator.  
  
## See Also  
 [MustInherit](../Topic/MustInherit%20\(Visual%20Basic\).md)   
 [New Operator](../vs140/New-Operator--Visual-Basic-.md)