---
title: "extent::operator-= Operator1"
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
H1: extent::operator/= Operator
ms.assetid: e044be0b-3ccd-4234-b299-308c69de6420
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# extent::operator-= Operator1
Divides each element in the [extent](../vs140/extent-Class--C---AMP-.md) object by the specified number.  
  
## Syntax  
  
```  
extent<_Rank>& operator/=(  
   int _Rhs  
) restrict(amp,cpu);  
```  
  
#### Parameters  
 `_Rhs`  
 The number to divide by.  
  
## Return Value  
 The `extent` object.  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [extent Structure](../vs140/extent-Class--C---AMP-.md)