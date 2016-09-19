---
title: "future::wait_until Method"
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
ms.assetid: bf7c0bb3-4263-4129-afaa-e82f5b17f9ed
caps.latest.revision: 7
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# future::wait_until Method
Blocks the current thread until the associated asynchronous state is *ready* or until after a specified time point.  
  
## Syntax  
  
```cpp  
template<class Clock, class Duration>  
   future_status wait_until(  
      const chrono::time_point<Clock, Duration>& Abs_time) const;  
```  
  
#### Parameters  
 `Abs_time`  
 A [chrono::time_point](../vs140/time_point-Class.md) object that specifies a time after which the thread can unblock.  
  
## Return Value  
 A [future_status](../vs140/future_status-Enumeration.md) that indicates the reason for returning.  
  
## Remarks  
 An associated asynchronous state is *ready* only if its asynchronous provider has stored a return value or stored an exception.  
  
## Requirements  
 **Header:** future  
  
 **Namespace:** std  
  
## See Also  
 [future Class](../vs140/future-Class.md)   
 [<future\>](../vs140/-future-.md)