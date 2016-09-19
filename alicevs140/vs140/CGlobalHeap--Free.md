---
title: "CGlobalHeap::Free"
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
ms.assetid: 63d79379-83ca-4f4b-a3a0-e6b8fc11a488
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CGlobalHeap::Free
Call this method to free a block of memory allocated by this memory manager.  
  
## Syntax  
  
```  
  
      virtual void Free(  
   void* p   
) throw( );  
```  
  
#### Parameters  
 `p`  
 Pointer to memory previously allocated by this memory manager. NULL is a valid value and does nothing.  
  
## Remarks  
 Implemented using [GlobalFree](http://msdn.microsoft.com/library/windows/desktop/aa366579).  
  
## Requirements  
 **Header:** atlmem.h  
  
## See Also  
 [CGlobalHeap Class](../vs140/CGlobalHeap-Class.md)   
 [CGlobalHeap::Allocate](../vs140/CGlobalHeap--Allocate.md)