---
title: "CAnimationController::CleanUpGroup"
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
ms.assetid: 1ece68a9-8616-47ef-a682-80a978cdc43b
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationController::CleanUpGroup
Called by the framework to clean up the group when animation has been scheduled.  
  
## Syntax  
  
```  
void CleanUpGroup(  
   UINT32 nGroupID  
);  
void CleanUpGroup(  
   CAnimationGroup* pGroup  
);  
```  
  
#### Parameters  
 `nGroupID`  
 Specifies GroupID.  
  
 `pGroup`  
 A pointer to animation group to clean.  
  
## Remarks  
 This method removes all transitions and keyframes from the specified group, because they are not relevant after an animation has been scheduled.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationController Class](../vs140/CAnimationController-Class.md)