---
title: "atomic::fetch_or Method"
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
ms.assetid: 4c532f7f-80c5-432a-b34b-48feacab8dca
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# atomic::fetch_or Method
Performs a bitwise `or` on a value and an existing value that is stored in `*this`.  
  
## Syntax  
  
```  
Ty atomic<Ty>::fetch_or (  
   Ty Value,  
   memory_order Order = memory_order_seq_cst  
) volatile _NOEXCEPT;  
Ty atomic<Ty>::fetch_or (  
   Ty Value,  
   memory_order Order = memory_order_seq_cst  
) _NOEXCEPT;  
```  
  
#### Parameters  
 `Value`  
 A value of type `Ty`.  
  
 `Order`  
 A [memory_order](../vs140/memory_order-Enum.md).  
  
## Return Value  
 A `Ty` object that contains the result of the bitwise `or`.  
  
## Remarks  
 The `fetch_or` method performs a `read-modify-write` operation to replace the stored value of `*this` with a bitwise `or` of `Value` and the current value that is stored in `*this`, within the memory constraints that are specified by `Order`.  
  
## Requirements  
 **Header:** atomic  
  
 **Namespace:** std  
  
## See Also  
 [<atomic\>](../vs140/-atomic-.md)   
 [atomic Structure](../vs140/atomic-Structure.md)   
 [atomic_fetch_or_explicit](../vs140/atomic_fetch_or_explicit-Function.md)