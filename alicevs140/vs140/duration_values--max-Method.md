---
title: "duration_values::max Method"
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
ms.assetid: 062e20c1-8c63-4492-ae8d-58fb8e5f6074
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# duration_values::max Method
Static method that returns the upper bound for values of type `Ref`.  
  
## Syntax  
  
```  
static constexpr Rep max();  
```  
  
## Return Value  
 In effect, returns `numeric_limits<Rep>::max()`.  
  
## Remarks  
 When `Rep` is a user-defined type, the return value must be greater than [duration_values::zero](../vs140/duration_values--zero-Method.md).  
  
## Requirements  
 **Header:** chrono  
  
 **Namespace:** std::chrono  
  
## See Also  
 [duration_values Structure](../vs140/duration_values-Structure.md)   
 [<chrono\>](../vs140/-chrono-.md)   
 [numeric_limits Class](../vs140/numeric_limits-Class.md)