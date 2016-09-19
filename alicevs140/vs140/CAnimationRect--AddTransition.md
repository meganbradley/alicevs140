---
title: "CAnimationRect::AddTransition"
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
ms.assetid: f3529081-ed50-451b-a787-ddad28a7cb35
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationRect::AddTransition
Adds transitions for left, top, right and bottom coordinates.  
  
## Syntax  
  
```  
void AddTransition(  
   CBaseTransition* pLeftTransition,  
   CBaseTransition* pTopTransition,  
   CBaseTransition* pRightTransition,  
   CBaseTransition* pBottomTransition  
);  
```  
  
#### Parameters  
 `pLeftTransition`  
 Specifies transition for the left side.  
  
 `pTopTransition`  
 Specifies transition for the top side.  
  
 `pRightTransition`  
 Specifies transition for the right side.  
  
 `pBottomTransition`  
 Specifies transition for the bottom side.  
  
## Remarks  
 Call this function to add the specified transitions to the internal list of transitions to be applied to animation variables for each rectangle sides. When you add transitions, they are not applied immediately and stored in an internal list. Transitions are applied (added to a storyboard for a particular value) when you call CAnimationController::AnimateGroup. If you don't need to apply a transition to one of the rectangle sides, you can pass NULL.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationRect Class](../vs140/CAnimationRect-Class.md)