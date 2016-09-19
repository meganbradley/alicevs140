---
title: "CBaseTransition::GetEndKeyframe"
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
ms.assetid: 59cdc55e-bb55-4466-a910-6e5b454b7b1c
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBaseTransition::GetEndKeyframe
Returns start keyframe.  
  
## Syntax  
  
```  
CBaseKeyFrame* GetEndKeyframe();  
```  
  
## Return Value  
 A valid pointer to a keyframe, or NULL if a transition should not be inserted between keyframes.  
  
## Remarks  
 This method can be used to access a keyframe object that was previously set by SetKeyframes. It's called by top level code when transitions are being added to storyboard.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CBaseTransition Class](../vs140/CBaseTransition-Class.md)