---
title: "nearbyintf Function"
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
ms.assetid: a22561a9-e569-4563-8a56-7d4db068d64b
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# nearbyintf Function
Rounds the argument to an integer value in floating-point format, using the current rounding direction.  
  
## Syntax  
  
```  
inline float nearbyintf(  
   float _X  
) restrict(amp);  
```  
  
#### Parameters  
 `_X`  
 Floating-point value  
  
## Return Value  
 Returns the rounded integer value.  
  
## Requirements  
 **Header:** amp_math.h  
  
 **Namespace:** Concurrency::precise_math  
  
## See Also  
 [Concurrency::precise_math Namespace](../vs140/Concurrency--precise_math-Namespace.md)