---
title: "extent::operator(mod)= Operator"
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
ms.assetid: c0a79fb9-d464-4cd6-9d86-85b8fc9198d1
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# extent::operator(mod)= Operator
Calculates the modulus (remainder) of each element in the [extent](../vs140/extent-Class--C---AMP-.md) when that element is divided by a number.  
  
## Syntax  
  
```  
extent<_Rank>& operator%=(  
   int _Rhs  
) restrict(cpu, direct3d);  
```  
  
#### Parameters  
 `_Rhs`  
 The number to find the modulus of.  
  
## Return Value  
 The `extent` object.  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [extent Structure](../vs140/extent-Class--C---AMP-.md)