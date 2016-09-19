---
title: "atomic::load Method"
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
ms.assetid: 05212726-cf8a-46fe-83d2-c16ac2abb7d1
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# atomic::load Method
Retrieves the stored value in `*this`, within the specified memory constraints.  
  
## Syntax  
  
```  
Ty atomic::load(  
   memory_order Order = memory_order_seq_cst  
) const volatile _NOEXCEPT;  
Ty atomic::load(  
   memory_order Order = memory_order_seq_cst  
) const _NOEXCEPT;  
```  
  
#### Parameters  
 `Order`  
 A [memory_order](../vs140/memory_order-Enum.md). Order must not be `memory_order_release` or `memory_order_acq_rel`.  
  
## Return Value  
 The retrieved value that is stored in `*this`.  
  
## Requirements  
 **Header:** atomic  
  
 **Namespace:** std  
  
## See Also  
 [<atomic\>](../vs140/-atomic-.md)   
 [atomic Structure](../vs140/atomic-Structure.md)   
 [atomic_load_explicit](../vs140/atomic_load_explicit-Function.md)