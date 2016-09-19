---
title: "operator- Operator (STL)1"
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
H1: operator- Operator (STL)
ms.assetid: a1602990-7cfc-4c56-9a87-676812e83a18
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# operator- Operator (STL)1
Operator for subtraction or negation of [duration](../vs140/duration-Class.md) and [time_point](../vs140/time_point-Class.md) objects.  
  
## Syntax  
  
```  
template<  
   class Rep1, class Period1,  
   class Rep2, class Period2>  
   constexpr typename common_type<  
      duration<Rep1, Period1>,   
      duration<Rep2, Period2> >::type  
   operator-(  
      const duration<Rep1, Period1>& Left,  
      const duration<Rep2, Period2>& Right);  
  
template<class Clock, class Duration1, class Rep2, class Period2>  
   constexpr time_point<Clock,   
      typename common_type<Duration1, duration<Rep2, Period2> >::type>   operator-(  
      const time_point<Clock, Duration1>& Time,  
      const duration<Rep2, Period2>& Dur);  
  
template<class Clock, class Duration1, class Duration2>  
   constexpr typename common_type<Duration1, Duration2>::type  
   operator-(  
      const time_point<Clock, Duration1>& Left,  
      const time_point<Clock, Duration2>& Right);  
```  
  
#### Parameters  
 `Left`  
 The left `duration` or `time_point` object.  
  
 `Right`  
 The right `duration` or `time_point` object.  
  
 `Time`  
 A `time_point` object.  
  
 `Dur`  
 A `duration` object.  
  
## Return Value  
 The first function returns a `duration` object whose interval length is the difference between the time intervals of the two arguments.  
  
 The second function returns a `time_point` object that represents a point in time that is displaced, by the negation of the time interval that is represented by `Dur`, from the point in time that is specified by `Time`.  
  
 The third function returns a `duration` object that represents the time interval between `Left` and `Right`.  
  
## Requirements  
 **Header:** chrono  
  
 **Namespace:** std::chrono  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)