---
title: "CSinusoidalTransitionFromRange::CSinusoidalTransitionFromRange"
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
ms.assetid: 775d68df-fa06-472b-9658-28556534d374
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSinusoidalTransitionFromRange::CSinusoidalTransitionFromRange
Constructs a transition object.  
  
## Syntax  
  
```  
CSinusoidalTransitionFromRange(  
   UI_ANIMATION_SECONDS duration,  
   DOUBLE dblMinimumValue,  
   DOUBLE dblMaximumValue,  
   UI_ANIMATION_SECONDS period,  
   UI_ANIMATION_SLOPE slope  
);  
```  
  
#### Parameters  
 `duration`  
 The duration of the transition.  
  
 `dblMinimumValue`  
 The value of the animation variable at a trough of the sinusoidal wave.  
  
 `dblMaximumValue`  
 The value of the animation variable at a peak of the sinusoidal wave.  
  
 `period`  
 The period of oscillation of the sinusoidal wave in seconds.  
  
 `slope`  
 The slope at the start of the transition.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CSinusoidalTransitionFromRange Class](../vs140/CSinusoidalTransitionFromRange-Class.md)