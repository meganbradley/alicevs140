---
title: "time_point::max Method"
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
ms.assetid: 9effc0c3-531c-4151-b81b-2c204f919756
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# time_point::max Method
Static method that returns the upper bound for values of type `time_point::ref`.  
  
## Syntax  
  
```  
static constexpr time_point max();  
```  
  
## Return Value  
 In effect, returns `time_point(duration::max())`.  
  
## Requirements  
 **Header:** chrono  
  
 **Namespace:** std::chrono  
  
## See Also  
 [time_point Class](../vs140/time_point-Class.md)   
 [duration::max](../vs140/duration--max-Method.md)   
 [<chrono\>](../vs140/-chrono-.md)