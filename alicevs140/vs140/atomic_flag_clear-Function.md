---
title: "atomic_flag_clear Function"
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
ms.assetid: 037f50bc-5c87-4e22-9757-92a175aec42c
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# atomic_flag_clear Function
Sets the `bool` flag in an [atomic_flag](../vs140/atomic_flag-Structure.md) object to `false`, within the `memory_order_seq_cst`[memory_order](../vs140/memory_order-Enum.md).  
  
## Syntax  
  
```  
inline void atomic_flag_clear(  
   volatile atomic_flag *Flag  
) _NOEXCEPT;  
inline void atomic_flag_clear(  
   atomic_flag *Flag  
) _NOEXCEPT;  
```  
  
#### Parameters  
 `Flag`  
 A pointer to an `atomic_flag` object.  
  
## Requirements  
 **Header:** atomic  
  
 **Namespace:** std  
  
## See Also  
 [<atomic\>](../vs140/-atomic-.md)