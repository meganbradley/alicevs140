---
title: "atomic::operator Ty Operator"
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
ms.assetid: a366c700-c7a0-4bcb-8eb4-4b57dfaea065
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# atomic::operator Ty Operator
Retrieves the stored value in `*this`.  
  
## Syntax  
  
```  
atomic<Ty>::operator Ty() const volatile _NOEXCEPT;  
atomic<Ty>::operator Ty() const _NOEXCEPT;  
```  
  
## Remarks  
 This operator applies the `memory_order_seq_cst`[memory_order](../vs140/memory_order-Enum.md).  
  
## Requirements  
 **Header:** atomic  
  
 **Namespace:** std  
  
## See Also  
 [<atomic\>](../vs140/-atomic-.md)   
 [atomic Structure](../vs140/atomic-Structure.md)   
 [atomic::load](../vs140/atomic--load-Method.md)