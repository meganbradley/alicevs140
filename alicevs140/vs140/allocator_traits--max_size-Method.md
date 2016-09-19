---
title: "allocator_traits::max_size Method"
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
ms.assetid: 728265ef-0df3-4538-913b-829c23012918
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# allocator_traits::max_size Method
Static method that uses a specified allocator to determine the maximum number of objects that can be allocated.  
  
## Syntax  
  
```cpp  
static size_type max_size(const Alloc& al);  
```  
  
#### Parameters  
 `al`  
 An allocator object.  
  
## Remarks  
 This method returns `al.max_size()`, if that expression is well formed; otherwise it returns `numeric_limits<size_type>::max()`.  
  
## Requirements  
 **Header:** <memory\>  
  
 **Namespace:** std  
  
## See Also  
 [allocator::max_size](../vs140/allocator--max_size.md)   
 [allocator_traits Class](../vs140/allocator_traits-Class.md)