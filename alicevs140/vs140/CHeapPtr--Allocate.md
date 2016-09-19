---
title: "CHeapPtr::Allocate"
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
ms.assetid: b8aa2f7a-4a97-4a0f-a3ec-148e5bff663c
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHeapPtr::Allocate
Call this method to allocate memory on the heap to store objects.  
  
## Syntax  
  
```  
  
      bool Allocate(  
   size_t nElements = 1   
) throw( );  
```  
  
#### Parameters  
 `nElements`  
 The number of elements used to calculate the amount of memory to allocate. The default value is 1.  
  
## Return Value  
 Returns true if the memory was successfully allocated, false on failure.  
  
## Remarks  
 The allocator routines are used to reserve enough memory on the heap to store *nElement* objects of a type defined in the constructor.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#77](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#77)]  
  
## Requirements  
 **Header:** atlalloc.h  
  
## See Also  
 [CHeapPtr Class](../vs140/CHeapPtr-Class.md)   
 [CHeapPtr::Reallocate](../vs140/CHeapPtr--Reallocate.md)