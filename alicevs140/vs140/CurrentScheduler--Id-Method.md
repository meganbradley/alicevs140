---
title: "CurrentScheduler::Id Method"
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
ms.assetid: 9f88a503-7edf-4b97-a83b-031b662df4f0
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CurrentScheduler::Id Method
Returns a unique identifier for the current scheduler.  
  
## Syntax  
  
```  
static unsigned int __cdecl Id();  
```  
  
## Return Value  
 If a scheduler is associated with the calling context, a unique identifier for that scheduler; otherwise, the value `-1`.  
  
## Remarks  
 This method will not result in scheduler attachment if the calling context is not already associated with a scheduler.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [CurrentScheduler Class](../vs140/CurrentScheduler-Class.md)