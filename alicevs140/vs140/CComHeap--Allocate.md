---
title: "CComHeap::Allocate"
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
ms.assetid: 70676059-be1c-4915-94a7-3ab39d4f202a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComHeap::Allocate
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
 Call [CComHeap::Free](../vs140/CComHeap--Free.md) or [CComHeap::Reallocate](../vs140/CComHeap--Reallocate.md) to free the memory allocated by this method.  
  
 Implemented using [CoTaskMemAlloc](http://msdn.microsoft.com/library/windows/desktop/ms692727).  
  
## Requirements  
 **Header:** atlcommem.h  
  
## See Also  
 [CComHeap Class](../vs140/CComHeap-Class.md)   
 [CComHeap::Free](../vs140/CComHeap--Free.md)   
 [CComHeap::Reallocate](../vs140/CComHeap--Reallocate.md)