---
title: "isfinite Function"
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
ms.assetid: 39d5ddcb-0f13-40a9-9f9e-50b74e44f31d
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# isfinite Function
Determines whether the argument has a finite value  
  
## Syntax  
  
```  
inline int isfinite(  
   float _X  
) restrict(amp);  
inline int isfinite(  
   double _X  
) restrict(amp);  
```  
  
#### Parameters  
 `_X`  
 Floating-point value  
  
## Return Value  
 Returns a nonzero value if and only if the argument has a finite value  
  
## Requirements  
 **Header:** amp_math.h  
  
 **Namespace:** Concurrency::precise_math  
  
## See Also  
 [Concurrency::precise_math Namespace](../vs140/Concurrency--precise_math-Namespace.md)