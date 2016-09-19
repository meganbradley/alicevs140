---
title: "CAnimationController::FindAnimationGroup"
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
ms.assetid: 66fed5f6-3188-4fcb-b567-168d286c569c
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationController::FindAnimationGroup
Finds an animation group by its Group ID.  
  
## Syntax  
  
```  
CAnimationGroup* FindAnimationGroup(  
   UINT32 nGroupID  
);  
CAnimationGroup* FindAnimationGroup(  
   IUIAnimationStoryboard* pStoryboard  
);  
```  
  
#### Parameters  
 `nGroupID`  
 Specifies a GroupID.  
  
 `pStoryboard`  
 A pointer to a storyboard.  
  
## Return Value  
 A pointer to animation group or NULL if the group with specified ID is not found.  
  
## Remarks  
 Use this method to find an animation group at runtime. A group is created and added to the internal list of animation groups when a first animation object with particular GroupID is being added to animation controller.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationController Class](../vs140/CAnimationController-Class.md)