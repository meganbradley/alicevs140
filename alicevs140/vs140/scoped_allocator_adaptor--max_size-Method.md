---
title: "scoped_allocator_adaptor::max_size Method"
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
ms.assetid: 45c164f3-c1e1-4a35-812a-fff0bcac7102
caps.latest.revision: 6
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# scoped_allocator_adaptor::max_size Method
Determines the maximum number of objects that can be allocated by the outer allocator.  
  
## Syntax  
  
```cpp  
size_type max_size();  
```  
  
## Return Value  
 `Outer_traits::max_size(outer_allocator())`  
  
## Requirements  
 **Header:** <scoped_allocator>  
  
 **Namespace:** std  
  
## See Also  
 [scoped_allocator_adaptor Class](../vs140/scoped_allocator_adaptor-Class.md)   
 [allocator_traits::max_size Method](../vs140/allocator_traits--max_size-Method.md)