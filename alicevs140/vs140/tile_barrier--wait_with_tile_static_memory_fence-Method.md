---
title: "tile_barrier::wait_with_tile_static_memory_fence Method"
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
ms.assetid: 65109506-63a0-4219-ae61-03974355c09c
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# tile_barrier::wait_with_tile_static_memory_fence Method
Blocks execution of all threads in a tile until all threads in a tile have reached this call. This ensures that `tile_static`memory accesses are visible to other threads in the thread tile, and have been executed in program order.  
  
## Syntax  
  
```  
void wait_with_tile_static_memory_fence() const restrict(amp);  
```  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [tile_barrier Class](../vs140/tile_barrier-Class.md)