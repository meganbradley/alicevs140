---
title: "fdim Function"
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
ms.assetid: 7b4622b2-1b61-4fed-b5af-c9bb0170af2f
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# fdim Function
Computes the positive difference between the arguments.  
  
## Syntax  
  
```  
inline float fdim(  
   float _X,  
   float _Y  
) restrict(amp);  
inline double fdim(  
   double _X,  
   double _Y  
) restrict(amp);  
```  
  
#### Parameters  
 `_X`  
 Floating-point value  
  
 `_Y`  
 Floating-point value  
  
## Return Value  
 The difference between `_X` and `_Y` if `_X` is greater than `_Y`; otherwise, `+0`.  
  
## Requirements  
 **Header:** amp_math.h  
  
 **Namespace:** Concurrency::precise_math  
  
## See Also  
 [Concurrency::precise_math Namespace](../vs140/Concurrency--precise_math-Namespace.md)