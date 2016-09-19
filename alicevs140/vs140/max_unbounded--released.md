---
title: "max_unbounded::released"
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
ms.assetid: 0d5c1568-d551-4a78-a0b7-f1a8de490fe8
caps.latest.revision: 9
translation.priority.mt: 
  - de-de
  - ja-jp
---
# max_unbounded::released
Decrements the count of memory blocks on the free list.  
  
## Syntax  
  
```  
void released();  
```  
  
## Remarks  
 This member function does nothing. The `released` member function of the current max class is called by `cache_freelist::allocate` whenever it removes a memory block from the free list.  
  
## Requirements  
 **Header:** <allocators\>  
  
 **Namespace:** stdext  
  
## See Also  
 [max_unbounded Class](../vs140/max_unbounded-Class.md)