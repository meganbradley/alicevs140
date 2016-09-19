---
title: "CBaseKeyFrame::GetAnimationKeyframe"
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
ms.assetid: 66360a07-8798-4c72-83ec-34a6f89dea3f
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBaseKeyFrame::GetAnimationKeyframe
Returns the underlying keyframe value.  
  
## Syntax  
  
```  
UI_ANIMATION_KEYFRAME GetAnimationKeyframe() const;  
```  
  
## Return Value  
 A current keyframe. The default value is UI_ANIMATION_KEYFRAME_STORYBOARD_START.  
  
## Remarks  
 This is an accessor to the underlying keyframe value.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CBaseKeyFrame Class](../vs140/CBaseKeyFrame-Class.md)