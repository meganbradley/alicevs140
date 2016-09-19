---
title: "system_clock Structure"
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
ms.assetid: a97bd46e-267a-4836-9f7d-af1f664e99ae
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# system_clock Structure
Represents a *clock type* that is based on the real-time clock of the system.  
  
## Syntax  
  
```  
struct system_clock;  
```  
  
## Remarks  
 A *clock type* is used to obtain the current time as UTC. The type embodies an instantiation of [duration](../vs140/duration-Class.md) and the class template [time_point](../vs140/time_point-Class.md), and defines a static member function `now()` that returns the time.  
  
 A clock is *monotonic* if the value that is returned by a first call to `now()` is always less than or equal to the value that is returned by a subsequent call to `now()`.  
  
 A clock is *steady* if it is *monotonic* and if the time between clock ticks is constant.  
  
 In this implementation, a `system_clock` is synonymous with a `high_resolution_clock`.  
  
## Members  
  
### Public Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|`system_clock::duration`|A synonym for `duration<rep, period>`.|  
|`system_clock::period`|A synonym for the type that is used to represent the tick period in the contained instantiation of `duration`.|  
|`system_clock::rep`|A synonym for the type that is used to represent the number of clock ticks in the contained instantiation of `duration`.|  
|`system_clock::time_point`|A synonym for `time_point<Clock, duration>`, where `Clock` is a synonym for either the clock type itself or another clock type that is based on the same epoch and has the same nested `duration` type.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[system_clock::from_time_t Method](#system_clock__from_time_t_method)|Static. Returns a `time_point` that most closely approximates a specified time.|  
|[system_clock::now Method](#system_clock__now_method)|Static. Returns the current time.|  
|[system_clock::to_time_t Method](#system_clock__to_time_t_method)|Static. Returns a `time_t` object that most closely approximates a specified `time_point`.|  
  
### Public Constants  
  
|Name|Description|  
|----------|-----------------|  
|[system_clock::is_monotonic Constant](#system_clock__is_monotonic_constant)|Specifies whether the clock type is monotonic.|  
|[system_clock::is_steady Constant](#system_clock__is_steady_constant)|Specifies whether the clock type is steady.|  
  
## Requirements  
 **Header:** chrono  
  
 **Namespace:** std::chrono  
  
##  <a name="system_clock__from_time_t_method"></a>  system_clock::from_time_t Method  
 Static method that returns a [time_point](../vs140/time_point-Class.md) that most closely approximates the time that is represented by `Tm`.  
  
```  
static time_point from_time_t(  
   time_t Tm  
) _NOEXCEPT;  
```  
  
### Parameters  
 `Tm`  
 A [time_t](../vs140/Standard-Types.md) object.  
  
##  <a name="system_clock__is_monotonic_constant"></a>  system_clock::is_monotonic Constant  
 Static value that specifies whether the clock type is monotonic.  
  
```  
static const bool is_monotonic = false;  
```  
  
### Return Value  
 In this implementation, `system_clock::is_monotonic` always returns `false`.  
  
### Remarks  
 A clock is *monotonic* if the value that is returned by a first call to `now()` is always less than or equal to the value that is returned by a subsequent call to `now()`.  
  
##  <a name="system_clock__is_steady_constant"></a>  system_clock::is_steady Constant  
 Static value that specifies whether the clock type is *steady*.  
  
```  
static const bool is_steady = false;  
```  
  
### Return Value  
 In this implementation, `system_clock::is_steady` always returns `false`.  
  
### Remarks  
 A clock is *steady* if it is [monotonic](#system_clock__is_monotonic_constant) and if the time between clock ticks is constant.  
  
##  <a name="system_clock__now_method"></a>  system_clock::now Method  
 Static method that returns the current time.  
  
```  
static time_point now() _NOEXCEPT;  
```  
  
### Return Value  
 A [time_point](../vs140/time_point-Class.md) object that represents the current time.  
  
##  <a name="system_clock__to_time_t_method"></a>  system_clock::to_time_t Method  
 Static method that returns a [time_t](../vs140/Standard-Types.md) that most closely approximates the time that is represented by `Time`.  
  
```  
static time_t to_time_t(  
   const time_point& Time  
) _NOEXCEPT;  
```  
  
### Parameters  
 `Time`  
 A [time_point](../vs140/time_point-Class.md) object.  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)   
 [<chrono\>](../vs140/-chrono-.md)   
 [steady_clock Class](../vs140/steady_clock-struct.md)