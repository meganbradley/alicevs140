---
title: "nanf Function"
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
ms.assetid: 82abb93e-5732-4148-b2da-7e1aec9c3d59
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# nanf Function
Returns a quiet NaN  
  
## Syntax  
  
```  
inline float nanf(  
   int _X  
) restrict(amp);  
```  
  
#### Parameters  
 `_X`  
 Integer value  
  
## Return Value  
 Returns a quiet NaN, if available, with the content indicated in _X  
  
## Requirements  
 **Header:** amp_math.h  
  
 **Namespace:** Concurrency::precise_math  
  
## See Also  
 [Concurrency::precise_math Namespace](../vs140/Concurrency--precise_math-Namespace.md)