---
title: "rcp Function"
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
ms.assetid: 4bed60c6-5b92-4b29-aa7f-cb7482cf32a8
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# rcp Function
Computes the reciprocal of the specified argument by using a fast approximation.  
  
## Syntax  
  
```  
inline float rcp(  
   float _X  
) restrict(amp);  
  
inline double rcp(  
   double _X  
) restrict(amp);  
```  
  
#### Parameters  
 `_X`  
 The value for which to compute the reciprocal.  
  
## Return Value  
 The reciprocal of the specified argument.  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency::direct3d  
  
## See Also  
 [Concurrency::direct3d Namespace](../vs140/Concurrency--direct3d-Namespace.md)