---
title: "logb Function"
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
ms.assetid: 633fb9be-963e-4e77-80cc-3811f1244b21
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# logb Function
Extracts the exponent of _X, as a signed integer value in floating-point format  
  
## Syntax  
  
```  
inline float logb(  
   float _X  
) restrict(amp);  
inline double logb(  
   double _X  
) restrict(amp);  
```  
  
#### Parameters  
 `_X`  
 Floating-point value  
  
## Return Value  
 Returns the signed exponent of _X  
  
## Requirements  
 **Header:** amp_math.h  
  
 **Namespace:** Concurrency::precise_math  
  
## See Also  
 [Concurrency::precise_math Namespace](../vs140/Concurrency--precise_math-Namespace.md)