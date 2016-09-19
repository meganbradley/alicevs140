---
title: "modf Function"
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
ms.assetid: 38823a15-e457-4813-8e55-8741fa3615ff
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# modf Function
Splits the specified argument into fractional and integer parts.  
  
## Syntax  
  
```  
inline float modf(  
   float _X,  
   _Out_ float * _Iptr  
) restrict(amp);  
inline double modf(  
   double _X,  
   _Out_ double * _Iptr  
) restrict(amp);  
```  
  
#### Parameters  
 `_X`  
 Floating-point value  
  
 `_Iptr` (out parameter)  
 The integer portion of `_X`, as a floating-point value.  
  
## Return Value  
 The signed fractional portion of `_X`.  
  
## Requirements  
 **Header:** amp_math.h  
  
 **Namespace:** Concurrency::precise_math  
  
## See Also  
 [Concurrency::precise_math Namespace](../vs140/Concurrency--precise_math-Namespace.md)