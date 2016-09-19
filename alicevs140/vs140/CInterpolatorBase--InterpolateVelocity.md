---
title: "CInterpolatorBase::InterpolateVelocity"
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
ms.assetid: 6836d64c-f45a-4d32-99ce-3cfcea65bad5
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CInterpolatorBase::InterpolateVelocity
Interpolates the velocity at a given offset  
  
## Syntax  
  
```  
IFACEMETHOD(  
   InterpolateVelocity  
)(__in UI_ANIMATION_SECONDS offset, __out DOUBLE *velocity);  
```  
  
#### Parameters  
 `offset`  
 The offset from the start of the transition. The offset is always greater than or equal to zero and less than or equal to the duration of the transition. This method is not called if the duration of the transition is zero.  
  
 `velocity`  
 Output. The velocity of the variable at the offset.  
  
## Return Value  
 If the method succeeds, it returns S_OK. It returns E_FAIL if CCustomInterpolator is not set, or custom implementation returns FALSE from the InterpolateVelocity method.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CInterpolatorBase Class](../vs140/CInterpolatorBase-Class.md)