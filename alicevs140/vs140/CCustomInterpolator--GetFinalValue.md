---
title: "CCustomInterpolator::GetFinalValue"
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
ms.assetid: 38345271-903b-4ef6-9776-2a595566ee36
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCustomInterpolator::GetFinalValue
Gets the final value to which the interpolator leads.  
  
## Syntax  
  
```  
virtual BOOL GetFinalValue(  
   DOUBLE *value  
);  
```  
  
#### Parameters  
 `value`  
 Output. The final value of a variable at the end of the transition.  
  
## Return Value  
 Basic implementation always returns TRUE. Return FALSE from overridden implementation if you wish to fail the event.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CCustomInterpolator Class](../vs140/CCustomInterpolator-Class.md)