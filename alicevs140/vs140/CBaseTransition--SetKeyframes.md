---
title: "CBaseTransition::SetKeyframes"
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
ms.assetid: f1b12db0-2ba6-4ba5-9e4e-eb51df499c65
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBaseTransition::SetKeyframes
Sets keyframes for a transition.  
  
## Syntax  
  
```  
void SetKeyframes(  
   CBaseKeyFrame* pStart = NULL,  
   CBaseKeyFrame* pEnd = NULL  
);  
```  
  
#### Parameters  
 `pStart`  
 A keyframe that specifies the beginning of the transition.  
  
 `pEnd`  
 A keyframe that specifies the end of the transition.  
  
## Remarks  
 This method tells the transition to start after specified keyframe and, optionally, if pEnd is not NULL, end before the specified keyframe. If the transition was created with a duration parameter specified, that duration is overwritten with the duration of time between the start and end keyframes.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CBaseTransition Class](../vs140/CBaseTransition-Class.md)