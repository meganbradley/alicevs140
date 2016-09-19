---
title: "freelist::pop"
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
ms.assetid: b9ca6e37-d996-455d-b44b-cbd8903bc316
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# freelist::pop
Removes the first memory block from the free list.  
  
## Syntax  
  
```  
void *pop();  
```  
  
## Return Value  
 Returns a pointer to the memory block removed from the list.  
  
## Remarks  
 The member function returns `NULL` if the list is empty. Otherwise, it removes the first memory block from the list.  
  
## Requirements  
 **Header:** <allocators\>  
  
 **Namespace:** stdext  
  
## See Also  
 [freelist Class](../vs140/freelist-Class.md)