---
title: "isinf Function (fast_math)"
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
ms.assetid: 14edf7ce-64c8-4e2b-afbf-7fd842e7b159
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# isinf Function (fast_math)
Determines whether the argument is an infinity  
  
## Syntax  
  
```  
inline int isinf(  
   float _X  
) restrict(amp);  
```  
  
#### Parameters  
 `_X`  
 Floating-point value  
  
## Return Value  
 Returns a nonzero value if and only if the argument has an infinite value  
  
## Requirements  
 **Header:** amp_math.h  
  
 **Namespace:** Concurrency::fast_math  
  
## See Also  
 [Concurrency::fast_math Namespace](../vs140/Concurrency--fast_math-Namespace.md)