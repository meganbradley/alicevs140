---
title: "CKeyFrame::AddToStoryboardAfterTransition"
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
ms.assetid: 3427b52b-9840-470a-b47b-bbb9184a4227
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CKeyFrame::AddToStoryboardAfterTransition
Adds a keyframe to storyboard after transition.  
  
## Syntax  
  
```  
BOOL AddToStoryboardAfterTransition(  
   IUIAnimationStoryboard* pStoryboard,  
   BOOL bDeepAdd  
);  
```  
  
#### Parameters  
 `pStoryboard`  
 A pointer to a storyboard.  
  
 `bDeepAdd`  
 Specifies whether to add a transition recursively.  
  
## Return Value  
 TRUE, if keyframe was added successfully.  
  
## Remarks  
 This function is called by the framework to add a keyframe to storyboard after transition.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CKeyFrame Class](../vs140/CKeyFrame-Class.md)