---
title: "CCustomInterpolator::SetDuration"
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
ms.assetid: 36254eec-b79c-411a-b5f5-a92c3b57eccb
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCustomInterpolator::SetDuration
Sets the interpolator's duration.  
  
## Syntax  
  
```  
virtual BOOL SetDuration(  
   UI_ANIMATION_SECONDS duration  
);  
```  
  
#### Parameters  
 `duration`  
 The duration of the transition.  
  
## Return Value  
 Basic implementation always returns TRUE. Return FALSE from overridden implementation if you wish to fail the event.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CCustomInterpolator Class](../vs140/CCustomInterpolator-Class.md)