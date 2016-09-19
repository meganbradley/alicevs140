---
title: "CAnimationPoint::operator CPoint"
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
ms.assetid: 7138141b-c9f3-4308-938f-3d59407d99df
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationPoint::operator CPoint
Converts a CAnimationPoint to a CPoint.  
  
## Syntax  
  
```  
operator CPoint();  
```  
  
## Return Value  
 Current value of CAnimationPoint as CPoint.  
  
## Remarks  
 This function internally calls GetValue. If GetValue for some reason fails, the returned point will contain default values for X and Y coordinates.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationPoint Class](../vs140/CAnimationPoint-Class.md)