---
title: "packaged_task::reset Method"
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
ms.assetid: e1d200e3-2117-4087-b60d-132a38f29bc5
caps.latest.revision: 7
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# packaged_task::reset Method
Uses a new *associated asynchronous state* to replace the existing associated asynchronous state.  
  
## Syntax  
  
```cpp  
void reset();  
```  
  
## Remarks  
 In effect, this method executes `*this = packaged_task(move(fn))`, where *fn* is the function object that's stored in the associated asynchronous state for this object. Therefore, the state of the object is cleared, and [get_future](../vs140/packaged_task--get_future-Method.md), [operator()](../vs140/packaged_task--operator---Operator.md), and [make_ready_at_thread_exit](../vs140/packaged_task--make_ready_at_thread_exit-Method.md) can be called as if on a newly-constructed object.  
  
## Requirements  
 **Header:** future  
  
 **Namespace:** std  
  
## See Also  
 [packaged_task Class](../vs140/packaged_task-Class.md)   
 [<future\>](../vs140/-future-.md)