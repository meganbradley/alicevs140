---
title: "mad Function"
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
ms.assetid: a51df420-ea6e-4ecb-bd1c-8334edc2ca7a
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# mad Function
Computes the product of the first and second specified argument, then adds the third specified argument.  
  
## Syntax  
  
```  
inline float mad(  
   float _X,  
   float _Y,  
   float _Z  
) restrict(amp);  
  
inline double mad(  
   double _X,  
   double _Y,  
   double _Z  
) restrict(amp);  
  
inline int mad(  
   int _X,  
   int _Y,  
   int _Z  
) restrict(amp);  
  
inline unsigned int mad(  
   unsigned int _X,  
   unsigned int _Y,  
   unsigned int _Z  
) restrict(amp);  
```  
  
#### Parameters  
 `_X`  
 The first specified argument.  
  
 `_Y`  
 The second specified argument.  
  
 `_Z`  
 The third specified argument.  
  
## Return Value  
 The result of `_X` * `_Y` + `_Z`.  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency::direct3d  
  
## See Also  
 [direct3d Namespace](../vs140/Concurrency--direct3d-Namespace.md)