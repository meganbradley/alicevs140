---
title: "CAnimationController::EnableAnimationTimerEventHandler"
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
ms.assetid: 9ea3d988-9da2-4baa-9977-eb5f889d0711
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationController::EnableAnimationTimerEventHandler
Sets or releases a handler for timing events and handler for timing updates.  
  
## Syntax  
  
```  
virtual BOOL EnableAnimationTimerEventHandler(  
   BOOL bEnable = TRUE,  
   UI_ANIMATION_IDLE_BEHAVIOR idleBehavior = UI_ANIMATION_IDLE_BEHAVIOR_DISABLE  
);  
```  
  
#### Parameters  
 `bEnable`  
 Specifies whether to set or release the handlers.  
  
 `idleBehavior`  
 Specifies idle behavior for timer update handler.  
  
## Return Value  
 TRUE if handlers were successfully set or released; FALSE if this method is called for a second time without releasing the handlers first, or if any other error occurs.  
  
## Remarks  
 When the handlers are set (enabled) Windows Animation API calls OnAnimationTimerPreUpdate, OnAnimationTimerPostUpdate, OnRenderingTooSlow methods. You need to enable animation timers to allow Windows Animation API update storyboards. Otherwise you'll need to call CAnimationController::UpdateAnimationManager in order to direct the animation manager to update the values of all animation variables.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationController Class](../vs140/CAnimationController-Class.md)