---
title: "sleep_until Function"
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
ms.assetid: fc6bc4eb-d957-4302-87a8-71d2d435596f
caps.latest.revision: 8
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# sleep_until Function
Blocks the calling thread at least until the specified time.  
  
## Syntax  
  
```  
template<class Clock, class Duration>  
    void sleep_until(const chrono::time_point<Clock, Duration>& Abs_time);  
void sleep_until(const xtime *Abs_time);  
```  
  
#### Parameters  
 `Abs_time`  
 Represents a point in time.  
  
## Remarks  
 This function does not throw any exceptions.  
  
## Requirements  
 **Header:** thread  
  
 **Namespace:** std::this_thread  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)   
 [<thread\>](../vs140/-thread-.md)   
 [time_point](../vs140/time_point-Class.md)