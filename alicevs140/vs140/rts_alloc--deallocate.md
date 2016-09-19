---
title: "rts_alloc::deallocate"
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
ms.topic: article
ms.assetid: 407f70e8-763d-4384-95a6-5b8ac8df7342
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# rts_alloc::deallocate
Frees a specified number of objects from storage beginning at a specified position.  
  
## Syntax  
  
```  
void deallocate(void* _Ptr, std::size_t _Count);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Ptr`|A pointer to the first object to be deallocated from storage.|  
|`_Count`|The number of objects to be deallocated from storage.|  
  
## Remarks  
 The member function calls `caches[_IDX].deallocate(_Ptr, _Count)`, where the index `_IDX` is determined by the requested block size `_Count`, or, if `_Count` is too large, it returns `operator delete(_Ptr)`.  
  
## Requirements  
 **Header:** <allocators\>  
  
 **Namespace:** stdext  
  
## See Also  
 [rts_alloc Class](../vs140/rts_alloc-Class.md)