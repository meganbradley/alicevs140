---
title: "max_unbounded::deallocated"
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
ms.assetid: 8f3d525c-5847-4c25-a6a7-51cab98a932a
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# max_unbounded::deallocated
Decrements the count of allocated memory blocks.  
  
## Syntax  
  
```  
void deallocated(std::size_t _Nx = 1);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Nx`|The increment value.|  
  
## Remarks  
 The member function does nothing. This member function is called after each call by `cache_freelist::deallocate` to operator `delete`. The argument `_Nx` is the number of memory blocks in the chunk deallocated by operator `delete`.  
  
## Requirements  
 **Header:** <allocators\>  
  
 **Namespace:** stdext  
  
## See Also  
 [max_unbounded Class](../vs140/max_unbounded-Class.md)