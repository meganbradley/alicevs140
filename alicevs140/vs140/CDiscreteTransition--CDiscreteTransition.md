---
title: "CDiscreteTransition::CDiscreteTransition"
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
ms.assetid: 08b42876-1982-43ed-8d35-7a43b01fa214
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDiscreteTransition::CDiscreteTransition
Constructs a discrete transition object and initializes its parameters.  
  
## Syntax  
  
```  
CDiscreteTransition(  
   UI_ANIMATION_SECONDS delay,  
   DOUBLE dblFinalValue,  
   UI_ANIMATION_SECONDS hold  
);  
```  
  
#### Parameters  
 `delay`  
 The amount of time by which to delay the instantaneous switch to the final value.  
  
 `dblFinalValue`  
 The value of the animation variable at the end of the transition.  
  
 `hold`  
 The amount of time by which to hold the variable at its final value.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CDiscreteTransition Class](../vs140/CDiscreteTransition-Class.md)