---
title: "timer::propagate_to_any_targets Method"
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
ms.assetid: 476737c0-2322-452e-b416-d0127f709590
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# timer::propagate_to_any_targets Method
Tries to offer the message produced by the `timer` block to all of the linked targets.  
  
## Syntax  
  
```  
virtual void propagate_to_any_targets(  
   _Inout_opt_ message<_Type> *  
);  
```  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [timer Class](../vs140/timer-Class.md)