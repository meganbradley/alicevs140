---
title: "CHeapPtr::Reallocate"
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
ms.assetid: de27f137-1c50-41d1-bf61-e8237202d404
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHeapPtr::Reallocate
Call this method to reallocate the memory on the heap.  
  
## Syntax  
  
```  
  
      bool Reallocate(  
   size_t nElements   
) throw( );  
```  
  
#### Parameters  
 `nElements`  
 The new number of elements used to calculate the amount of memory to allocate.  
  
## Return Value  
 Returns true if the memory was successfully allocated, false on failure.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#79](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#79)]  
  
## Requirements  
 **Header:** atlalloc.h  
  
## See Also  
 [CHeapPtr Class](../vs140/CHeapPtr-Class.md)   
 [CHeapPtr::Allocate](../vs140/CHeapPtr--Allocate.md)