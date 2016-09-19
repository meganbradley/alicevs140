---
title: "CCRTHeap::Allocate"
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
ms.topic: reference
ms.assetid: dc479d19-5bb8-4a84-93a4-8dcfdaf0770f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCRTHeap::Allocate
Call this method to allocate a block of memory.  
  
## Syntax  
  
```  
  
      virtual __declspec(allocator) void* Allocate(  
   size_t nBytes   
) throw( );  
```  
  
#### Parameters  
 `nBytes`  
 The requested number of bytes in the new memory block.  
  
## Return Value  
 Returns a pointer to the start of the newly allocated memory block.  
  
## Remarks  
 Call [CCRTHeap::Free](../vs140/CCRTHeap--Free.md) or [CCRTHeap::Reallocate](../vs140/CCRTHeap--Reallocate.md) to free the memory allocated by this method.  
  
 Implemented using [malloc](../vs140/malloc.md).  
  
## Requirements  
 **Header:** atlmem.h  
  
## See Also  
 [CCRTHeap Class](../vs140/CCRTHeap-Class.md)   
 [CCRTHeap::Reallocate](../vs140/CCRTHeap--Reallocate.md)   
 [CCRTHeap::Free](../vs140/CCRTHeap--Free.md)