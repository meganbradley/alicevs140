---
title: "CBaseKeyFrame::AddToStoryboard"
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
ms.assetid: b126405f-a833-43ad-aea2-91f3ea7bef94
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBaseKeyFrame::AddToStoryboard
Adds a keyframe to storyboard.  
  
## Syntax  
  
```  
virtual BOOL AddToStoryboard(  
   IUIAnimationStoryboard* pStoryboard,  
   BOOL bDeepAdd  
);  
```  
  
#### Parameters  
 `pStoryboard`  
 A pointer to a storyboard.  
  
 `bDeepAdd`  
 If this parameter is TRUE and the keyframe being added depends on some other keyframe or transition, this method tries to add this keyframe or transition to storyboard first.  
  
## Return Value  
 TRUE if keyframe was added to storyboard successfully; otherwise FALSE.  
  
## Remarks  
 This method is called to add a keyframe to storyboard.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CBaseKeyFrame Class](../vs140/CBaseKeyFrame-Class.md)