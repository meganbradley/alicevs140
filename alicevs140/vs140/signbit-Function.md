---
title: "signbit Function"
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
ms.assetid: 661a217d-f7dc-46e8-8585-2c37cbcae3a9
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# signbit Function
Determines whether the sign of _X is negative  
  
## Syntax  
  
```  
inline int signbit(  
   float _X  
) restrict(amp);  
inline int signbit(  
   double _X  
) restrict(amp);  
```  
  
#### Parameters  
 `_X`  
 Floating-point value  
  
## Return Value  
 Returns a nonzero value if and only if the sign of _X is negative  
  
## Requirements  
 **Header:** amp_math.h  
  
 **Namespace:** Concurrency::precise_math  
  
## See Also  
 [Concurrency::precise_math Namespace](../vs140/Concurrency--precise_math-Namespace.md)