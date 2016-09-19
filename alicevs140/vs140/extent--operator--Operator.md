---
title: "extent::operator- Operator"
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
ms.assetid: 0dc56971-8639-410f-a9c2-aaaffb8302f3
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# extent::operator- Operator
Creates a new `extent` object by subtracting each element in the specified `index` object from the corresponding element in this `extent` object.  
  
## Syntax  
  
```  
extent<_Rank> operator-(  
   const index<_Rank>& _Rhs  
) restrict(amp,cpu);  
```  
  
#### Parameters  
 `_Rhs`  
 The `index` object that contains the elements to subtract.  
  
## Return Value  
 The new `extent` object.  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [extent Structure](../vs140/extent-Class--C---AMP-.md)