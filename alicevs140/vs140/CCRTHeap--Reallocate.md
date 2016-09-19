---
title: "CCRTHeap::Reallocate"
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
ms.assetid: 0e978038-4fcf-4b6e-b9ce-69ea50fe55f8
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCRTHeap::Reallocate
Call this method to reallocate memory allocated by this memory manager.  
  
## Syntax  
  
```  
  
      virtual __declspec(allocator) void* Reallocate(  
   void* p,  
   size_t nBytes   
) throw( );  
```  
  
#### Parameters  
 `p`  
 Pointer to memory previously allocated by this memory manager.  
  
 `nBytes`  
 The requested number of bytes in the new memory block.  
  
## Return Value  
 Returns a pointer to the start of the newly allocated memory block.  
  
## Remarks  
 Call [CCRTHeap::Free](../vs140/CCRTHeap--Free.md) to free the memory allocated by this method. Implemented using [realloc](../vs140/realloc.md).  
  
## Requirements  
 **Header:** atlmem.h  
  
## See Also  
 [CCRTHeap Class](../vs140/CCRTHeap-Class.md)   
 [CCRTHeap::Allocate](../vs140/CCRTHeap--Allocate.md)   
 [CCRTHeap::Free](../vs140/CCRTHeap--Free.md)