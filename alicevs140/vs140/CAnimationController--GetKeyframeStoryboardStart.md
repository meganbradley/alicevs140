---
title: "CAnimationController::GetKeyframeStoryboardStart"
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
ms.assetid: 936830a6-2571-4e50-a72a-fd56db16ddba
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationController::GetKeyframeStoryboardStart
Returns a keyframe that identifies start of storyboard.  
  
## Syntax  
  
```  
static CBaseKeyFrame* GetKeyframeStoryboardStart();  
```  
  
## Return Value  
 A pointer to base keyframe, which identifies start of storyboard.  
  
## Remarks  
 Obtain this keyframe to base any other keyframes or transitions on the moment in time when a storyboard starts.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationController Class](../vs140/CAnimationController-Class.md)