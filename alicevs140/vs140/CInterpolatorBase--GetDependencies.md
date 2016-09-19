---
title: "CInterpolatorBase::GetDependencies"
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
ms.assetid: d2290372-c8ca-407d-94ff-21ef15e50895
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CInterpolatorBase::GetDependencies
Gets the interpolator's dependencies.  
  
## Syntax  
  
```  
IFACEMETHOD(  
   GetDependencies  
)(__out UI_ANIMATION_DEPENDENCIES *initialValueDependencies, __out UI_ANIMATION_DEPENDENCIES *initialVelocityDependencies, __out UI_ANIMATION_DEPENDENCIES *durationDependencies);  
```  
  
#### Parameters  
 `initialValueDependencies`  
 Output. Aspects of the interpolator that depend on the initial value passed to SetInitialValueAndVelocity.  
  
 `initialVelocityDependencies`  
 Output. Aspects of the interpolator that depend on the initial velocity passed to SetInitialValueAndVelocity.  
  
 `durationDependencies`  
 Output. Aspects of the interpolator that depend on the duration passed to SetDuration.  
  
## Return Value  
 If the method succeeds, it returns S_OK. It returns E_FAIL if CCustomInterpolator is not set, or custom implementation returns FALSE from the GetDependencies method.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CInterpolatorBase Class](../vs140/CInterpolatorBase-Class.md)