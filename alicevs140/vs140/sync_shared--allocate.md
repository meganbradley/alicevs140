---
title: "sync_shared::allocate"
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
ms.assetid: 5573ad54-bdd1-4019-ba13-7e291d5c9f79
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# sync_shared::allocate
Allocates a block of memory.  
  
## Syntax  
  
```  
void *allocate(std::size_t _Count);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Count`|The number of elements in the array to be allocated.|  
  
## Return Value  
 A pointer to the allocated object.  
  
## Remarks  
 The member function locks the mutex, calls `cache.allocate(_Count)`, unlocks the mutex, and returns the result of the earlier call to `cache.allocate(_Count)`. `cache` represents the current cache object.  
  
## Requirements  
 **Header:** <allocators\>  
  
 **Namespace:** stdext  
  
## See Also  
 [sync_shared Class](../vs140/sync_shared-Class.md)