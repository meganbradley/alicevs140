---
title: "CCRTAllocator::Allocate"
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
ms.assetid: cc5f1db2-28ed-4961-a01b-0505160eaec2
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCRTAllocator::Allocate
Call this static function to allocate memory.  
  
## Syntax  
  
```  
  
      static __declspec(allocator) void* Allocate(  
   size_t nBytes   
) throw( );  
```  
  
#### Parameters  
 `nBytes`  
 The number of bytes to allocate.  
  
## Return Value  
 Returns a void pointer to the allocated space, or NULL if there is insufficient memory available.  
  
## Remarks  
 Allocates memory. See [malloc](../vs140/malloc.md) for more details.  
  
## Requirements  
 **Header:** atlalloc.h  
  
## See Also  
 [CCRTAllocator Class](../vs140/CCRTAllocator-Class.md)   
 [CCRTAllocator::Reallocate](../vs140/CCRTAllocator--Reallocate.md)   
 [CCRTAllocator::Free](../vs140/CCRTAllocator--Free.md)