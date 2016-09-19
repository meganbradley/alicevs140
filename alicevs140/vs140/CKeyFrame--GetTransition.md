---
title: "CKeyFrame::GetTransition"
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
ms.assetid: bd5d145b-0987-4bd1-a1fb-56e50d3c7a13
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CKeyFrame::GetTransition
Returns a pointer to a transition this keyframe depends on.  
  
## Syntax  
  
```  
CBaseTransition* GetTransition();  
```  
  
## Return Value  
 A valid pointer to transition, or NULL if this keyframe does not depend on transition.  
  
## Remarks  
 This is an accessor to a transition this keyframe depends on.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CKeyFrame Class](../vs140/CKeyFrame-Class.md)