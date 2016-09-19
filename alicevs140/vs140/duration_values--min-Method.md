---
title: "duration_values::min Method"
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
ms.assetid: cad76427-acc2-471c-95f6-1ec770495b9e
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# duration_values::min Method
Static method that returns the lower bound for values of type `Ref`.  
  
## Syntax  
  
```  
static constexpr Rep min();  
```  
  
## Return Value  
 In effect, returns `numeric_limits<Rep>::lowest()`.  
  
## Remarks  
 When `Rep` is a user-defined type, the return value must be less than or equal to [duration_values::zero](../vs140/duration_values--zero-Method.md).  
  
## Requirements  
 **Header:** chrono  
  
 **Namespace:** std::chrono  
  
## See Also  
 [duration_values Structure](../vs140/duration_values-Structure.md)   
 [<chrono\>](../vs140/-chrono-.md)   
 [numeric_limits Class](../vs140/numeric_limits-Class.md)