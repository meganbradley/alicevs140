---
title: "allocator_base::allocator_base"
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
ms.assetid: 6f0d2a5b-fa0d-4d5e-ac06-80928de0b359
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# allocator_base::allocator_base
Constructs an object of type `allocator_base`.  
  
## Syntax  
  
```  
allocator_base();  
template <class Other>  
    allocator_base(const allocator_base<Other, Sync>& _Right);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Right`|The allocator object to be copied.|  
  
## Remarks  
 The first constructor constructs an [allocator_base](../vs140/allocator_base-Class.md) instance. The second constructor constructs an `allocator_base` instance such that for any `allocator_base<Type, _Sync>` instance `a`, `allocator_base<Type, Sync>(allocator_base<Other, Sync>(a)) == a`.  
  
## Requirements  
 **Header:** <allocators\>  
  
 **Namespace:** stdext  
  
## See Also  
 [allocator_base](../vs140/allocator_base-Class.md)