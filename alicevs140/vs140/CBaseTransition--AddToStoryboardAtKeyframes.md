---
title: "CBaseTransition::AddToStoryboardAtKeyframes"
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
ms.assetid: 51eaf9df-43ad-457b-8f3e-91f7b58fff3d
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBaseTransition::AddToStoryboardAtKeyframes
Adds a transition to a storyboard.  
  
## Syntax  
  
```  
BOOL AddToStoryboardAtKeyframes(  
   IUIAnimationStoryboard* pStoryboard  
);  
```  
  
#### Parameters  
 `pStoryboard`  
 A pointer to storyboard, which will animate the related variable.  
  
## Return Value  
 TRUE, if transition was successfully added to a storyboard.  
  
## Remarks  
 Applies the transition to the related variable in the storyboard. If the start keyframe was specified, the transition begins at that keyframe. If the end keyframe was specified, the transition begins at the start keyframe and and stops at the end keyframe. If the transition was created with a duration parameter specified, that duration is overwritten with the duration of time between the start and end keyframes. If no keyframe was specified, the transition is appended to the transition added most recently to the variable.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CBaseTransition Class](../vs140/CBaseTransition-Class.md)