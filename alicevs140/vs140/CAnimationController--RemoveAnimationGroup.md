---
title: "CAnimationController::RemoveAnimationGroup"
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
ms.assetid: 9b5b6ec2-7acd-4f15-a66f-3f018a4c0f4f
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationController::RemoveAnimationGroup
Removes an animation group with specified ID from animation controller.  
  
## Syntax  
  
```  
void RemoveAnimationGroup(  
   UINT32 nGroupID  
);  
```  
  
#### Parameters  
 `nGroupID`  
 Specifies animation group ID.  
  
## Remarks  
 This method removes an animation group from the internal list of groups and deletes it, therefore if you stored a pointer to that animation group, it must be invalidated. If CAnimationGroup::m_bAutodestroyAnimationObjects is TRUE, all animation objects that belong to that group will be deleted; otherwise their references to parent animation controller will be set to NULL and they can be added to another controller.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationController Class](../vs140/CAnimationController-Class.md)