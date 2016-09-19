---
title: "max_variable_size::full"
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
ms.assetid: c2b15915-4bbf-4ec9-a4e7-b8eec1f7561d
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# max_variable_size::full
Returns a value that specifies whether more memory blocks should be added to the free list.  
  
## Syntax  
  
```  
bool full();  
```  
  
## Return Value  
 `true` if `_Nallocs / 16 + 16 <= _Nblocks`.  
  
## Remarks  
 This member function is called by `cache_freelist::deallocate`. If the call returns `true`, `deallocate` puts the memory block on the free list; if it returns false, `deallocate` calls operator `delete` to deallocate the block.  
  
## Requirements  
 **Header:** <allocators\>  
  
 **Namespace:** stdext  
  
## See Also  
 [max_variable_size Class](../vs140/max_variable_size-Class.md)