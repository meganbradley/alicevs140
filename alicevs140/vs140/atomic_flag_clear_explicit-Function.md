---
title: "atomic_flag_clear_explicit Function"
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
ms.assetid: e1147db5-0a11-4261-bcbb-bcecf070ee15
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# atomic_flag_clear_explicit Function
Sets the `bool` flag in an [atomic_flag](../vs140/atomic_flag-Structure.md) object to `false`, within the specified [memory_order](../vs140/memory_order-Enum.md) constraints.  
  
## Syntax  
  
```  
inline void atomic_flag_clear_explicit(  
   volatile atomic_flag *Flag,  
   memory_order Order  
) _NOEXCEPT;  
inline void atomic_flag_clear_explicit(  
   atomic_flag *Flag,  
   memory_order Order  
) _NOEXCEPT;  
```  
  
#### Parameters  
 `Flag`  
 A pointer to an `atomic_flag` object.  
  
 `Order`  
 A [memory_order](../vs140/memory_order-Enum.md).  
  
## Requirements  
 **Header:** atomic  
  
 **Namespace:** std  
  
## See Also  
 [<atomic\>](../vs140/-atomic-.md)