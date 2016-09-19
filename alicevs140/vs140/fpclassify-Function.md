---
title: "fpclassify Function"
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
ms.assetid: 28c1d518-c48c-42c8-aa19-f429703d9286
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# fpclassify Function
Classifies the argument value as NaN, infinite, normal, subnormal, zero  
  
## Syntax  
  
```  
inline int fpclassify(  
   float _X  
) restrict(amp);  
inline int fpclassify(  
   double _X  
) restrict(amp);  
```  
  
#### Parameters  
 `_X`  
 Floating-point value  
  
## Return Value  
 Returns the value of the number classification macro appropriate to the value of the argument.  
  
## Requirements  
 **Header:** amp_math.h  
  
 **Namespace:** Concurrency::precise_math  
  
## See Also  
 [Concurrency::precise_math Namespace](../vs140/Concurrency--precise_math-Namespace.md)