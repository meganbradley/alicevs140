---
title: "remainder Function"
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
ms.assetid: d8524e61-8c33-4a76-b201-5866c257c576
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# remainder Function
Computes the remainder: _X REM _Y  
  
## Syntax  
  
```  
inline float remainder(  
   float _X,  
   float _Y  
) restrict(amp);  
inline double remainder(  
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
 Returns _X REM _Y  
  
## Requirements  
 **Header:** amp_math.h  
  
 **Namespace:** Concurrency::precise_math  
  
## See Also  
 [Concurrency::precise_math Namespace](../vs140/Concurrency--precise_math-Namespace.md)