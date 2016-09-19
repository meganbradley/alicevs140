---
title: "CKeyFrame::GetExistingKeyframe"
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
ms.assetid: 48e435c0-21be-4010-8a1e-03536936aba9
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CKeyFrame::GetExistingKeyframe
Returns a pointer to a keyframe this keyframe depends on.  
  
## Syntax  
  
```  
CBaseKeyFrame* GetExistingKeyframe();  
```  
  
## Return Value  
 A valid pointer to keyframe, or NULL if this keyframe does not depend on other keyframe.  
  
## Remarks  
 This is an accessor to a keyframe this keyframe depends on.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CKeyFrame Class](../vs140/CKeyFrame-Class.md)