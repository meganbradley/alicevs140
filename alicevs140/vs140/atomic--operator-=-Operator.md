---
title: "atomic::operator-= Operator"
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
ms.assetid: 902d0d9f-88fd-4500-aa2d-1e50f443e77c
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# atomic::operator-= Operator
Subtracts a specified value from the stored value. Used only by integral and pointer specializations.  
  
## Syntax  
  
```  
Ty atomic<Ty>::operator-=(  
   Ty Value  
) volatile _NOEXCEPT;  
Ty atomic<Ty>::operator-=(  
   Ty Value  
) _NOEXCEPT;  
```  
  
#### Parameters  
 Value  
 An integral or pointer value.  
  
## Return Value  
 A `Ty` object that contains the result of the subtraction.  
  
## Remarks  
 This operator uses the `memory_order_seq_cst`[memory_order](../vs140/memory_order-Enum.md).  
  
## Requirements  
 **Header:** atomic  
  
 **Namespace:** std  
  
## See Also  
 [atomic Structure](../vs140/atomic-Structure.md)   
 [<atomic\>](../vs140/-atomic-.md)   
 [atomic_fetch_sub_explicit](../vs140/atomic_fetch_sub_explicit-Function.md)