---
title: "ldexp Function"
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
ms.assetid: 9a0299ef-cb0e-40f3-b371-da226d733954
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ldexp Function
Computes a real number from the specified mantissa and exponent.  
  
## Syntax  
  
```  
inline float ldexp(  
   float _X,  
   int _Exp  
) restrict(amp);  
inline double ldexp(  
   double _X,  
   double _Exp  
) restrict(amp);  
```  
  
#### Parameters  
 `_X`  
 Floating-point value, mantissa  
  
 `_Exp`  
 Integer value, exponent  
  
## Return Value  
 Returns _X * 2^_Exp  
  
## Requirements  
 **Header:** amp_math.h  
  
 **Namespace:** Concurrency::precise_math  
  
## See Also  
 [Concurrency::precise_math Namespace](../vs140/Concurrency--precise_math-Namespace.md)