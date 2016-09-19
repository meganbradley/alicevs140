---
title: "time_point::min Method"
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
ms.assetid: 47b224c7-6add-45a3-bdd9-3372ae45555c
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# time_point::min Method
Static method that returns the lower bound for values of type `time_point::ref`.  
  
## Syntax  
  
```  
static constexpr time_point min();  
```  
  
## Return Value  
 In effect, returns `time_point(duration::min())`.  
  
## Requirements  
 **Header:** chrono  
  
 **Namespace:** std::chrono  
  
## See Also  
 [time_point Class](../vs140/time_point-Class.md)   
 [duration::min](../vs140/duration--min-Method.md)   
 [<chrono\>](../vs140/-chrono-.md)