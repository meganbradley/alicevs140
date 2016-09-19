---
title: "CCustomInterpolator::InterpolateValue"
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
ms.assetid: 7778f750-f7f7-47f0-8135-1551bf23276a
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCustomInterpolator::InterpolateValue
Interpolates the value at a given offset.  
  
## Syntax  
  
```  
virtual BOOL InterpolateValue(  
   UI_ANIMATION_SECONDS */,  
   DOUBLE *value  
);  
```  
  
#### Parameters  
 `value`  
 Output. The interpolated value.  
  
## Return Value  
 Basic implementation always returns TRUE. Return FALSE from overridden implementation if you wish to fail the event.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CCustomInterpolator Class](../vs140/CCustomInterpolator-Class.md)