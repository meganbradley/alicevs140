---
title: "CSmoothStopTransition::CSmoothStopTransition"
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
ms.assetid: be763800-f064-4d8c-a2c8-f4e69d21b0e1
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSmoothStopTransition::CSmoothStopTransition
Constructs a smooth-stop transition and initializes its maximum duration and final value.  
  
## Syntax  
  
```  
CSmoothStopTransition(  
   UI_ANIMATION_SECONDS maximumDuration,  
   DOUBLE dblFinalValue  
);  
```  
  
#### Parameters  
 `maximumDuration`  
 The maximum duration of the transition.  
  
 `dblFinalValue`  
 The value of the animation variable at the end of the transition.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CSmoothStopTransition Class](../vs140/CSmoothStopTransition-Class.md)