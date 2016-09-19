---
title: "CAnimationController::AddKeyframeToGroup"
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
ms.assetid: 0b58961b-c534-44ff-9cc6-5abb66556313
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationController::AddKeyframeToGroup
Adds a keyframe to group.  
  
## Syntax  
  
```  
BOOL AddKeyframeToGroup(  
   UINT32 nGroupID,  
   CBaseKeyFrame* pKeyframe  
);  
```  
  
#### Parameters  
 `nGroupID`  
 Specifies Group ID.  
  
 `pKeyframe`  
 A pointer to a keyframe.  
  
## Return Value  
 TRUE if the function succeeds; otherwise FALSE.  
  
## Remarks  
 Usually you don't need to call this method, use CAnimationController::CreateKeyframe instead, which creates and adds the created keyframe to a group automatically.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationController Class](../vs140/CAnimationController-Class.md)