---
title: "promise::promise Constructor"
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
ms.assetid: 65fc9d4b-d9ef-4c64-b3eb-f212c12085e6
caps.latest.revision: 8
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# promise::promise Constructor
Constructs a `promise` object.  
  
## Syntax  
  
```  
promise();  
template<class Alloc>  
promise(  
   allocator_arg_t,  
   const Alloc& Al  
);  
promise(  
   promise&& Other  
) _NOEXCEPT;  
```  
  
#### Parameters  
 `Al`  
 A memory allocator. See [<allocators\>](../vs140/-allocators-.md) for more information.  
  
 `Other`  
 A `promise` object.  
  
## Remarks  
 The first constructor constructs an *empty*`promise` object.  
  
 The second constructor constructs an empty `promise` object and uses `Al` for memory allocation.  
  
 The third constructor constructs a `promise` object and transfers the associated asynchronous state from `Other`, and leaves `Other` empty.  
  
## Requirements  
 **Header:** future  
  
 **Namespace:** std  
  
## See Also  
 [promise Class](../vs140/promise-Class.md)   
 [<future\>](../vs140/-future-.md)