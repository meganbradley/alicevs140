---
title: "tile_static_memory_fence Function"
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
ms.assetid: 9d144a14-9b89-4764-8583-ae99194c6488
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# tile_static_memory_fence Function
Blocks execution of all threads in a tile until all outstanding `tile_static` memory accesses have been completed. This ensures that `tile_static` memory accesses are visible to other threads in the thread tile, and that accesses are executed in program order.  
  
## Syntax  
  
```  
inline void tile_static_memory_fence(  
   const tile_barrier & _Barrier  
) restrict(amp);  
```  
  
#### Parameters  
 `_Barrier`  
 A tile_barrier object.  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency::direct3d  
  
## See Also  
 [direct3d Namespace](../vs140/Concurrency--direct3d-Namespace.md)