---
title: "CInterpolatorBase::GetDuration"
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
ms.assetid: a5170323-c4a2-4e48-ba33-001fdaaf1c28
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CInterpolatorBase::GetDuration
Gets the interpolator's duration.  
  
## Syntax  
  
```  
IFACEMETHOD(  
   GetDuration  
)(__out UI_ANIMATION_SECONDS *duration);  
```  
  
#### Parameters  
 `duration`  
 Output. The duration of the transition, in seconds.  
  
## Return Value  
 If the method succeeds, it returns S_OK. It returns E_FAIL if CCustomInterpolator is not set, or custom implementation returns FALSE from the GetDuration method.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CInterpolatorBase Class](../vs140/CInterpolatorBase-Class.md)