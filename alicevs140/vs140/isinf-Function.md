---
title: "isinf Function"
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
ms.assetid: 69c0c41a-5002-4a5c-9815-181131e2deb5
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# isinf Function
Determines whether the argument is an infinity  
  
## Syntax  
  
```  
inline int isinf(  
   float _X  
) restrict(amp);  
inline int isinf(  
   double _X  
) restrict(amp);  
```  
  
#### Parameters  
 `_X`  
 Floating-point value  
  
## Return Value  
 Returns a nonzero value if and only if the argument has an infinite value  
  
## Requirements  
 **Header:** amp_math.h  
  
 **Namespace:** Concurrency::precise_math  
  
## See Also  
 [Concurrency::precise_math Namespace](../vs140/Concurrency--precise_math-Namespace.md)