---
title: "CCustomInterpolator::GetDuration"
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
ms.assetid: 26cc64c8-6a44-42a0-ab81-935c1bec9146
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCustomInterpolator::GetDuration
Gets the interpolator's duration.  
  
## Syntax  
  
```  
virtual BOOL GetDuration(  
   UI_ANIMATION_SECONDS *duration  
);  
```  
  
#### Parameters  
 `duration`  
 Output. The duration of the transition, in seconds.  
  
## Return Value  
 Basic implementation always returns TRUE. Return FALSE from overridden implementation if you wish to fail the event.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CCustomInterpolator Class](../vs140/CCustomInterpolator-Class.md)