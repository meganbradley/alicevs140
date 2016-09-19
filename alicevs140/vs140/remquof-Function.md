---
title: "remquof Function"
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
ms.assetid: 9153e983-84d0-4dcb-9278-f389bfd5d828
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# remquof Function
Computes the remainder of the first specified argument divided by the second specified argument. Also computes the quotient of the significand of the first specified argument divided by the significand of the second specified argument, and returns the quotient using the location specified in the third argument.  
  
## Syntax  
  
```  
inline float remquof(  
   float _X,  
   float _Y,  
   _Out_ int * _Quo  
) restrict(amp);  
```  
  
#### Parameters  
 `_X`  
 The first floating-point argument.  
  
 `_Y`  
 The second floating-point argument.  
  
 `_Quo` (out parameter)  
 The address of an integer that’s used to return the quotient of the fractional bits of `_X` divided by the fractional bits of `_Y`.  
  
## Return Value  
 Returns the remainder of `_X` divided by `_Y`.  
  
## Remarks  
 The quotient of the significands of _X and _Y returned in the location specified by _Quo is given the same sign as the entire value of _X divided by the entire value of _Y. The significands include the implicit most-significant bit, together with the explicit lower-order bits.  
  
## Requirements  
 **Header:** amp_math.h  
  
 **Namespace:** Concurrency::precise_math  
  
## See Also  
 [Concurrency::precise_math Namespace](../vs140/Concurrency--precise_math-Namespace.md)