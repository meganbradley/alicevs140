---
title: "make_choice Function"
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
ms.assetid: 98c33b3f-e8e5-4302-ba91-b56515c00066
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# make_choice Function
Constructs a `choice` messaging block from an optional `Scheduler` or `ScheduleGroup` and two or more input sources.  
  
## Syntax  
  
```  
template<  
   typename _Type1,  
   typename _Type2,  
   typename... _Types  
>  
choice<std::tuple<_Type1, _Type2, _Types...>> make_choice(  
   Scheduler& _PScheduler,  
   _Type1_Item1,  
   _Type2_Item2,  
   _Types... _Items  
);  
  
template<  
   typename _Type1,  
   typename _Type2,  
   typename... _Types  
>  
choice<std::tuple<_Type1, _Type2, _Types...>> make_choice(  
   ScheduleGroup& _PScheduleGroup,  
   _Type1_Item1,  
   _Type2_Item2,  
   _Types... _Items  
);  
  
template<  
   typename _Type1,  
   typename _Type2,  
   typename... _Types  
>  
choice<std::tuple<_Type1, _Type2, _Types...>> make_choice(  
   _Type1_Item1,  
   _Type2_Item2,  
   _Types... _Items  
);  
```  
  
#### Parameters  
 `_Type1`  
 The message block type of the first source.  
  
 `_Type2`  
 The message block type of the second source.  
  
 `_PScheduler`  
 The `Scheduler` object within which the propagation task for the `choice` messaging block is scheduled.  
  
 `_Item1`  
 The first source.  
  
 `_Item2`  
 The second source.  
  
 `_Items`  
 Additional sources.  
  
 `_PScheduleGroup`  
 The `ScheduleGroup` object within which the propagation task for the `choice` messaging block is scheduled. The `Scheduler` object used is implied by the schedule group.  
  
## Return Value  
 A `choice` message block with two or more input sources.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [choice Class](../vs140/choice-Class.md)   
 [Scheduler Class](../vs140/Scheduler-Class.md)   
 [ScheduleGroup Class](../vs140/ScheduleGroup-Class.md)