---
title: "ldexp Function (fast_math)"
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
ms.assetid: 29e2052b-341f-4d68-8b87-af5f5026c16b
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ldexp Function (fast_math)
Computes a real number from the mantissa and exponent  
  
## Syntax  
  
```  
inline float ldexp(  
   float _X,  
   int _Exp  
) restrict(amp);  
```  
  
#### Parameters  
 `_X`  
 Floating-point value, mentissa  
  
 `_Exp`  
 Integer exponent  
  
## Return Value  
 Returns _X * 2^_Exp  
  
## Requirements  
 **Header:** amp_math.h  
  
 **Namespace:** Concurrency::fast_math  
  
## See Also  
 [Concurrency::fast_math Namespace](../vs140/Concurrency--fast_math-Namespace.md)