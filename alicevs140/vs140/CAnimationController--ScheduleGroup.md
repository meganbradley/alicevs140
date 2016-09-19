---
title: "CAnimationController::ScheduleGroup"
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
ms.assetid: 9b3fdc85-8416-4b2a-9f8d-65807f65abe1
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationController::ScheduleGroup
Schedules an animation.  
  
## Syntax  
  
```  
BOOL ScheduleGroup(  
   UINT32 nGroupID,  
   UI_ANIMATION_SECONDS time = 0.0  
);  
```  
  
#### Parameters  
 `nGroupID`  
 Specifies animation Group ID to schedule.  
  
 `time`  
 Specifies time to schedule.  
  
## Return Value  
 TRUE if animation was scheduled successfully. FALSE if storyboard has not been created, or other error occurs.  
  
## Remarks  
 You must call AnimateGroup with parameter bScheduleNow set to FALSE prior ScheduleGroup. You can specify the desired animation time obtained from IUIAnimationTimer::GetTime. If the time parameter is 0.0, the animation is scheduled for the current time.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationController Class](../vs140/CAnimationController-Class.md)