---
title: "CWin32Heap::Reallocate"
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
ms.assetid: d1a3bb41-85a6-4ffd-ac1c-79728e9764bf
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWin32Heap::Reallocate
Reallocates a block of memory from the heap object.  
  
## Syntax  
  
```  
  
      virtual __declspec(allocator) void* Reallocate(  
   void* p,  
   size_t nBytes   
) throw( );  
```  
  
#### Parameters  
 `p`  
 Pointer to the block of memory to reallocate.  
  
 `nBytes`  
 The new size in bytes of the allocated block. The block can be made larger or smaller.  
  
## Return Value  
 Returns a pointer to the newly allocated memory block.  
  
## Remarks  
 If `p` is NULL, it's assumed that the memory block has not yet been allocated and [CWin32Heap::Allocate](../vs140/CWin32Heap--Allocate.md) is called, with an argument of `nBytes`.  
  
## Requirements  
 **Header:** atlmem.h  
  
## See Also  
 [CWin32Heap Class](../vs140/CWin32Heap-Class.md)   
 [HeapReAlloc](http://msdn.microsoft.com/library/windows/desktop/aa366704)   
 [CWin32Heap::Allocate](../vs140/CWin32Heap--Allocate.md)   
 [CWin32Heap::Free](../vs140/CWin32Heap--Free.md)