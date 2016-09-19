---
title: "atomic::operator++ Operator"
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
ms.assetid: 492959e9-1ea8-4e02-a031-82b1b92e91a0
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# atomic::operator++ Operator
Increments the stored value. Used only by integral and pointer specializations.  
  
## Syntax  
  
```  
Ty atomic<Ty>::operator++(int) volatile _NOEXCEPT;  
Ty atomic<Ty>::operator++(int) _NOEXCEPT;  
Ty atomic<Ty>::operator++() volatile _NOEXCEPT;  
Ty atomic<Ty>::operator++() _NOEXCEPT;  
```  
  
## Return Value  
 The first two operators return the incremented value; the last two operators return the value before the increment. The operators use the `memory_order_seq_cst`[memory_order](../vs140/memory_order-Enum.md).  
  
## Requirements  
 **Header:** atomic  
  
 **Namespace:** std  
  
## See Also  
 [atomic Structure](../vs140/atomic-Structure.md)   
 [<atomic\>](../vs140/-atomic-.md)   
 [atomic_fetch_add_explicit](../vs140/atomic_fetch_add_explicit-Function.md)