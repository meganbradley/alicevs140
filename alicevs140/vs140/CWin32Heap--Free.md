---
title: "CWin32Heap::Free"
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
ms.assetid: 20862464-6e36-4e53-87cd-9de268bd9879
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWin32Heap::Free
Frees memory previously allocated from the heap by [CWin32Heap::Allocate](../vs140/CWin32Heap--Allocate.md) or [CWin32Heap::Reallocate](../vs140/CWin32Heap--Reallocate.md).  
  
## Syntax  
  
```  
  
      virtual void Free(  
   void* p   
) throw( );  
```  
  
#### Parameters  
 `p`  
 Pointer to the block of memory to free. NULL is a valid value and does nothing.  
  
## Requirements  
 **Header:** atlmem.h  
  
## See Also  
 [CWin32Heap Class](../vs140/CWin32Heap-Class.md)   
 [CWin32Heap::Allocate](../vs140/CWin32Heap--Allocate.md)   
 [CWin32Heap::Reallocate](../vs140/CWin32Heap--Reallocate.md)   
 [HeapFree](http://msdn.microsoft.com/library/windows/desktop/aa366701)