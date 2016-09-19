---
title: "CCustomInterpolator::CCustomInterpolator"
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
ms.assetid: c9c8b922-f2ba-4071-a5c5-2191fa5a6fa1
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCustomInterpolator::CCustomInterpolator
Constructs a custom interpolator object and sets all values to default 0.  
  
## Syntax  
  
```  
CCustomInterpolator();  
CCustomInterpolator(  
   UI_ANIMATION_SECONDS duration,  
   DOUBLE finalValue  
);  
```  
  
#### Parameters  
 `duration`  
 The duration of the transition.  
  
 `finalValue`  
  
## Remarks  
 Use CCustomInterpolator::Init to initialize duration and final value later in the code.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CCustomInterpolator Class](../vs140/CCustomInterpolator-Class.md)