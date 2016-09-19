---
title: "packaged_task::packaged_task Constructor"
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
ms.assetid: d2dcaeb9-15b1-4a71-bbb1-1f3669ea0f6c
caps.latest.revision: 8
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# packaged_task::packaged_task Constructor
Constructs a `packaged_task` object.  
  
## Syntax  
  
```cpp  
packaged_task() noexcept;  
packaged_task(packaged_task&& Right) noexcept;  
template<class Fn>  
   explicit packaged_task(Fn&& fn);  
template<class Fn, class Alloc>  
   explicit packaged_task(allocator_arg_t,  
      const Alloc& alloc, Fn&& fn);  
```  
  
#### Parameters  
 `Right`  
 A `packaged_task` object.  
  
 `alloc`  
 A memory allocator. For more information, see [<allocators\>](../vs140/-allocators-.md).  
  
 `fn`  
 A function object.  
  
## Remarks  
 The first constructor constructs a `packaged_task` object that has no *associated asynchronous state*.  
  
 The second constructor constructs a `packaged_task` object and transfers the associated asynchronous state from `Right`. After the operation, `Right` no longer has an associated asynchronous state.  
  
 The third constructor constructs a `packaged_task` object that has a copy of `fn` stored in its associated asynchronous state.  
  
 The fourth constructor constructs a `packaged_task` object that has a copy of `fn` stored in its associated asynchronous state, and uses `alloc` for memory allocation.  
  
## Requirements  
 **Header:** future  
  
 **Namespace:** std  
  
## See Also  
 [packaged_task Class](../vs140/packaged_task-Class.md)   
 [<future\>](../vs140/-future-.md)