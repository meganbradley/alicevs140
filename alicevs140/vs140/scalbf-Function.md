---
title: "scalbf Function"
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
ms.assetid: dac95563-379e-4693-b1b5-978dad53f9a7
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# scalbf Function
Multiplies _X by FLT_RADIX to the power _Y  
  
## Syntax  
  
```  
inline float scalbf(  
   float _X,  
   float _Y  
) restrict(amp);  
```  
  
#### Parameters  
 `_X`  
 Floating-point value  
  
 `_Y`  
 Floating-point value  
  
## Return Value  
 Returns _X * (FLT_RADIX ^ _Y)  
  
## Requirements  
 **Header:** amp_math.h  
  
 **Namespace:** Concurrency::precise_math  
  
## See Also  
 [Concurrency::precise_math Namespace](../vs140/Concurrency--precise_math-Namespace.md)