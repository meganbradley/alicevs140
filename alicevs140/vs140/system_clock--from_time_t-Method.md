---
title: "system_clock::from_time_t Method"
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
ms.assetid: fadead84-420b-4b07-9339-1abdff250f3a
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# system_clock::from_time_t Method
Static method that returns a [time_point](../vs140/time_point-Class.md) that most closely approximates the time that is represented by `Tm`.  
  
## Syntax  
  
```  
static time_point from_time_t(  
   time_t Tm  
) _NOEXCEPT;  
```  
  
#### Parameters  
 `Tm`  
 A [time_t](../vs140/Standard-Types.md) object.  
  
## Requirements  
 **Header:** chrono  
  
 **Namespace:** std::chrono  
  
## See Also  
 [system_clock Structure](../vs140/system_clock-Structure.md)   
 [<chrono\>](../vs140/-chrono-.md)   
 [system_clock::to_time_t Method](../vs140/system_clock--to_time_t-Method.md)