---
title: "tile_barrier::wait_with_all_memory_fence Method"
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
ms.assetid: 2116d010-fdbb-4eea-af46-de3d82276932
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# tile_barrier::wait_with_all_memory_fence Method
Blocks execution of all threads in a tile until all threads in a tile have reached this call. This ensures that all memory accesses are visible to other threads in the thread tile, and have been executed in program order.  
  
## Syntax  
  
```  
void wait_with_all_memory_fence() const restrict(amp);  
```  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [tile_barrier Class](../vs140/tile_barrier-Class.md)