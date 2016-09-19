---
title: "array::get_extent Method"
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
ms.assetid: 624f2d27-3d2b-44b4-803a-403bf124b57d
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# array::get_extent Method
Returns the [extent](../vs140/extent-Class--C---AMP-.md) object of the [array](../vs140/array-Class.md).  
  
## Syntax  
  
```  
Concurrency::extent<_Rank> get_extent() const restrict(amp,cpu);  
```  
  
## Return Value  
 The `extent` object of the [array](../vs140/array-Class.md).  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [array Class](../vs140/array-Class.md)