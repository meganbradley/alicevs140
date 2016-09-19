---
title: "isnan Function"
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
ms.assetid: c1654e14-65ad-4a13-8c0d-c9e26ae759e5
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# isnan Function
Determines whether the argument is a NaN  
  
## Syntax  
  
```  
inline int isnan(  
   float _X  
) restrict(amp);  
inline int isnan(  
   double _X  
) restrict(amp);  
```  
  
#### Parameters  
 `_X`  
 Floating-point value  
  
## Return Value  
 Returns a nonzero value if and only if the argument has a NaN value  
  
## Requirements  
 **Header:** amp_math.h  
  
 **Namespace:** Concurrency::precise_math  
  
## See Also  
 [Concurrency::precise_math Namespace](../vs140/Concurrency--precise_math-Namespace.md)