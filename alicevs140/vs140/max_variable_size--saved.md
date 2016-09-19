---
title: "max_variable_size::saved"
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
ms.assetid: d856f204-fa94-4699-b96e-dde8f13424d9
caps.latest.revision: 9
translation.priority.mt: 
  - de-de
  - ja-jp
---
# max_variable_size::saved
Increments the count of memory blocks on the free list.  
  
## Syntax  
  
```  
void saved();  
```  
  
## Remarks  
 This member function increments the stored value `_Nblocks`. This member function is called by `cache_freelist::deallocate` whenever it puts a memory block on the free list.  
  
## Requirements  
 **Header:** <allocators\>  
  
 **Namespace:** stdext  
  
## See Also  
 [max_variable_size Class](../vs140/max_variable_size-Class.md)