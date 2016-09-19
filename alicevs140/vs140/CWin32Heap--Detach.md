---
title: "CWin32Heap::Detach"
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
ms.assetid: dcb3d1f4-a030-4716-a7be-5aeb4e488bee
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWin32Heap::Detach
Detaches the heap object from an existing heap.  
  
## Syntax  
  
```  
  
HANDLE Detach( ) throw( );  
  
```  
  
## Return Value  
 Returns the handle to the heap to which the object was previously attached.  
  
## Requirements  
 **Header:** atlmem.h  
  
## See Also  
 [CWin32Heap Class](../vs140/CWin32Heap-Class.md)   
 [CWin32Heap::Attach](../vs140/CWin32Heap--Attach.md)