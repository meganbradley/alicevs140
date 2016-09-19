---
title: "CWin32Heap::GetSize"
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
ms.assetid: d3569dfe-9ece-4021-825a-1c1327aab8f7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWin32Heap::GetSize
Returns the size of a memory block allocated from the heap object.  
  
## Syntax  
  
```  
  
      virtual size_t GetSize(  
   void* p   
) throw( );  
```  
  
#### Parameters  
 `p`  
 Pointer to the memory block whose size the method will obtain. This is a pointer returned by [CWin32Heap::Allocate](../vs140/CWin32Heap--Allocate.md) or [CWin32Heap::Reallocate](../vs140/CWin32Heap--Reallocate.md).  
  
## Return Value  
 Returns the size, in bytes, of the allocated memory block.  
  
## Requirements  
 **Header:** atlmem.h  
  
## See Also  
 [CWin32Heap Class](../vs140/CWin32Heap-Class.md)   
 [HeapSize](http://msdn.microsoft.com/library/windows/desktop/aa366706)