---
title: "operator!= Operator (STL)"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 86c9b109-42c7-497b-8a25-e5dc61ab8d3c
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# operator!= Operator (STL)
Inequality operator for [duration](../vs140/duration-Class.md) or [time_point](../vs140/time_point-Class.md) objects.  
  
## Syntax  
  
```  
template<class Rep1, class Period1, class Rep2, class Period2>  
   constexpr bool operator!=(  
      const duration<Rep1, Period1>& Left,  
      const duration<Rep2, Period2>& Right);  
  
template<class Clock, class Duration1, class Duration2>  
   constexpr bool operator!=(  
      const time_point<Clock, Duration1>& Left,  
      const time_point<Clock, Duration2>& Right);  
```  
  
#### Parameters  
 `Left`  
 The left `duration` or `time_point` object.  
  
 `Right`  
 The right `duration` or `time_point` object.  
  
## Return Value  
 Each function returns `!(Left == Right)`.  
  
## Requirements  
 **Header:** chrono  
  
 **Namespace:** std::chrono  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)   
 [<chrono\>](../vs140/-chrono-.md)