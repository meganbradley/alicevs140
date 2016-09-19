---
title: "atomic_flag_test_and_set_explicit Function"
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
ms.assetid: b96c55ec-1706-4036-8e67-e9e31e585d91
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# atomic_flag_test_and_set_explicit Function
Sets the `bool` flag in an [atomic_flag](../vs140/atomic_flag-Structure.md) object to `true`, within the specified [memory_order](../vs140/memory_order-Enum.md) constraints.  
  
## Syntax  
  
```  
inline bool atomic_flag_test_and_set_explicit(  
   volatile atomic_flag *Flag,  
   memory_order Order  
) _NOEXCEPT;  
inline bool atomic_flag_test_and_set_explicit(  
   atomic_flag *Flag,  
   memory_order Order  
) _NOEXCEPT;  
```  
  
#### Parameters  
 `Flag`  
 A pointer to an `atomic_flag` object.  
  
 `Order`  
 A [memory_order](../vs140/memory_order-Enum.md).  
  
## Return Value  
 The initial value of `Flag`.  
  
## Requirements  
 **Header:** atomic  
  
 **Namespace:** std  
  
## See Also  
 [<atomic\>](../vs140/-atomic-.md)