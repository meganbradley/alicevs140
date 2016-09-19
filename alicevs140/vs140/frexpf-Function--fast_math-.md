---
title: "frexpf Function (fast_math)"
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
ms.assetid: 685995c3-b055-4e8d-a74b-7f799563822d
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# frexpf Function (fast_math)
Gets the mantissa and exponent of _X  
  
## Syntax  
  
```  
inline float frexpf(  
   float _X,  
   _Out_ int * _Exp  
) restrict(amp);  
```  
  
#### Parameters  
 `_X`  
 Floating-point value  
  
 `_Exp`  
 Returns the integer exponent of _X in floating-point value  
  
## Return Value  
 Returns the mantissa _X  
  
## Requirements  
 **Header:** amp_math.h  
  
 **Namespace:** Concurrency::fast_math  
  
## See Also  
 [Concurrency::fast_math Namespace](../vs140/Concurrency--fast_math-Namespace.md)