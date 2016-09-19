---
title: "CParabolicTransitionFromAcceleration::CParabolicTransitionFromAcceleration"
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
ms.topic: reference
ms.assetid: 63ead035-025f-42e1-99d7-47675ec3ae73
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CParabolicTransitionFromAcceleration::CParabolicTransitionFromAcceleration
Constructs a parabolic-acceleration transition and initializes it with specified parameters.  
  
## Syntax  
  
```  
CParabolicTransitionFromAcceleration(  
   DOUBLE dblFinalValue,  
   DOUBLE dblFinalVelocity,  
   DOUBLE dblAcceleration  
);  
```  
  
#### Parameters  
 `dblFinalValue`  
 The value of the animation variable at the end of the transition.  
  
 `dblFinalVelocity`  
 The velocity of the animation variable at the end of the transition.  
  
 `dblAcceleration`  
 The acceleration of the animation variable during the transition.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CParabolicTransitionFromAcceleration Class](../vs140/CParabolicTransitionFromAcceleration-Class.md)