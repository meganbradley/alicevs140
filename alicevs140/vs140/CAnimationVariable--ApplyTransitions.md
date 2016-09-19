---
title: "CAnimationVariable::ApplyTransitions"
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
ms.assetid: eb1667d1-109e-4a22-88de-191712234261
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationVariable::ApplyTransitions
Adds transitions from the internal list to storyboard.  
  
## Syntax  
  
```  
void ApplyTransitions(  
   CAnimationController* pController,  
   IUIAnimationStoryboard* pStoryboard,  
   BOOL bDependOnKeyframes  
);  
```  
  
#### Parameters  
 `pController`  
 A pointer to parent animation controller.  
  
 `pStoryboard`  
 A pointer to storyboard.  
  
 `bDependOnKeyframes`  
 TRUE, if this method should add transitions that depend on keyframes.  
  
## Remarks  
 This method adds transitions from the internal list to storyboard. It's called from the top level code several times to add transitions that do not depend on keyframes and add transitions that depend on keyframes. If the underlying animation variable COM object has not been created, this method creates it at this stage.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationVariable Class](../vs140/CAnimationVariable-Class.md)