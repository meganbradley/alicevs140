---
title: "system_clock::to_time_t Method"
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
ms.assetid: b9a5df14-ecf2-407c-a8dd-9456a94b1da1
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# system_clock::to_time_t Method
Static method that returns a [time_t](../vs140/Standard-Types.md) that most closely approximates the time that is represented by `Time`.  
  
## Syntax  
  
```  
static time_t to_time_t(  
   const time_point& Time  
) _NOEXCEPT;  
```  
  
#### Parameters  
 `Time`  
 A [time_point](../vs140/time_point-Class.md) object.  
  
## Requirements  
 **Header:** chrono  
  
 **Namespace:** std::chrono  
  
## See Also  
 [system_clock Structure](../vs140/system_clock-Structure.md)   
 [<chrono\>](../vs140/-chrono-.md)   
 [system_clock::from_time_t Method](../vs140/system_clock--from_time_t-Method.md)