---
title: "index::operator(mod)= Operator"
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
ms.assetid: f36dd4b7-0815-4e70-b5a9-7f8d81995b8a
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# index::operator(mod)= Operator
Calculates the modulus (remainder) of each element in the [index](../vs140/index-Class.md) object when that element is divided by the specified number.  
  
## Syntax  
  
```  
index<_Rank>& operator%=(  
   int _Rhs  
) restrict(cpu, amp);  
```  
  
#### Parameters  
 `_Rhs`  
 The number to divide by to find the modulus.  
  
## Return Value  
 The [index](../vs140/index-Class.md) object.  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [index Structure](../vs140/index-Class.md)