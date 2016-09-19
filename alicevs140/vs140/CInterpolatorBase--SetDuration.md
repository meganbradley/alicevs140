---
title: "CInterpolatorBase::SetDuration"
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
ms.assetid: 435b18da-b11e-45cf-9fd8-43fd192c6a10
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CInterpolatorBase::SetDuration
Sets the interpolator's duration  
  
## Syntax  
  
```  
IFACEMETHOD(  
   SetDuration  
)(__in UI_ANIMATION_SECONDS duration);  
```  
  
#### Parameters  
 `duration`  
 The duration of the transition.  
  
## Return Value  
 If the method succeeds, it returns S_OK. It returns E_FAIL if CCustomInterpolator is not set, or custom implementation returns FALSE from the SetDuration method.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CInterpolatorBase Class](../vs140/CInterpolatorBase-Class.md)