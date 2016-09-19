---
title: "modff Function (fast_math)"
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
ms.assetid: ec72a38b-234a-4f6b-b20f-8531f938254b
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# modff Function (fast_math)
Splits _X into fractional and integer parts.  
  
## Syntax  
  
```  
inline float modff(  
   float _X,  
   float * _Ip  
) restrict(amp);  
```  
  
#### Parameters  
 `_X`  
 Floating-point value  
  
 `_Ip`  
  
## Return Value  
 Returns the signed fractional portion of _X  
  
## Requirements  
 **Header:** amp_math.h  
  
 **Namespace:** Concurrency::fast_math  
  
## See Also  
 [Concurrency::fast_math Namespace](../vs140/Concurrency--fast_math-Namespace.md)