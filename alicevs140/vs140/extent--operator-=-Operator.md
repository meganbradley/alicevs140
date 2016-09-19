---
title: "extent::operator*= Operator"
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
ms.assetid: 1d6c9274-c384-4bbb-ac3c-a68187dcff60
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# extent::operator*= Operator
Multiplies each element in the [extent](../vs140/extent-Class--C---AMP-.md) object by the specified number.  
  
## Syntax  
  
```  
extent<_Rank>& operator*=(  
   int _Rhs  
) restrict(amp,cpu);  
```  
  
#### Parameters  
 `_Rhs`  
 The number to multiply.  
  
## Return Value  
 The `extent` object.  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [extent Structure](../vs140/extent-Class--C---AMP-.md)