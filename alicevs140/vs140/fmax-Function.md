---
title: "fmax Function"
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
ms.assetid: d45483d0-70ab-4873-b76b-58b9e8d3af71
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# fmax Function
Determine the maximum numeric value of the arguments  
  
## Syntax  
  
```  
inline float fmax(  
   float _X,  
   float _Y  
) restrict(amp);  
inline double fmax(  
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
 Return the maximum numeric value of the arguments  
  
## Requirements  
 **Header:** amp_math.h  
  
 **Namespace:** Concurrency::precise_math  
  
## See Also  
 [Concurrency::precise_math Namespace](../vs140/Concurrency--precise_math-Namespace.md)