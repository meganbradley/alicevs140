---
title: "max_none::full"
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
ms.assetid: fc44210e-e45b-47c1-a247-8adc7153c4e8
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# max_none::full
Returns a value that specifies whether more memory blocks should be added to the free list.  
  
## Syntax  
  
```  
bool full();  
```  
  
## Return Value  
 This member function always returns `true`.  
  
## Remarks  
 This member function is called by `cache_freelist::deallocate`. If the call returns `true`, `deallocate` puts the memory block on the free list; if it returns false, `deallocate` calls operator `delete` to deallocate the block.  
  
## Requirements  
 **Header:** <allocators\>  
  
 **Namespace:** stdext  
  
## See Also  
 [max_none Class](../vs140/max_none-Class.md)