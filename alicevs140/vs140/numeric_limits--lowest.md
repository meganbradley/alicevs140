---
title: "numeric_limits::lowest"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e07443dc-9a2d-431e-8a00-c5a98295064e
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# numeric_limits::lowest
Returns the most negative finite value.  
  
## Syntax  
  
```  
static Type lowest() throw();  
```  
  
## Return Value  
 Returns the most negative finite value.  
  
## Remarks  
 Returns the most negative finite value for the type (which is typically `min` `()` for integer types and `-``max` `()` for floating-point types). The return value is meaningful if `is_bounded` is `true`.  
  
## Requirements  
 **Header:** <limits\>  
  
 **Namespace:** std  
  
## See Also  
 [numeric_limits Class](../vs140/numeric_limits-Class.md)   
 [<limits\>](../vs140/-limits-.md)