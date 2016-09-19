---
title: "allocator_base::max_size"
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
ms.assetid: 4739f5fa-42f4-4c19-954c-4e4e9c350e0d
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# allocator_base::max_size
Returns the number of elements of type `Type` that could be allocated by an object of class allocator before the free memory is used up.  
  
## Syntax  
  
```  
size_type max_size() const;  
```  
  
## Return Value  
 The number of elements that could be allocated.  
  
## Remarks  
 This member function is implemented for the user-defined allocator by returning `(size_t)-1 / sizeof(Type)` if `0 < (size_t)-1 / sizeof(Type)`, otherwise `1`.  
  
## Requirements  
 **Header:** <allocators\>  
  
 **Namespace:** stdext  
  
## See Also  
 [allocator_base Class](../vs140/allocator_base-Class.md)