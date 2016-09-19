---
title: "CWin32Heap::Allocate"
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
ms.assetid: 8725049a-9427-4794-b2be-984de88713c0
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWin32Heap::Allocate
Allocates a block of memory from the heap object.  
  
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
 Returns a pointer to the newly allocated memory block.  
  
## Remarks  
 Call [CWin32Heap::Free](../vs140/CWin32Heap--Free.md) or [CWin32Heap::Reallocate](../vs140/CWin32Heap--Reallocate.md) to free the memory allocated by this method.  
  
 Implemented using [HeapAlloc](http://msdn.microsoft.com/library/windows/desktop/aa366597).  
  
## Requirements  
 **Header:** atlmem.h  
  
## See Also  
 [CWin32Heap Class](../vs140/CWin32Heap-Class.md)