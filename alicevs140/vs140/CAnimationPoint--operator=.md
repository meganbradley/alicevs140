---
title: "CAnimationPoint::operator="
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
ms.assetid: 5cbdf398-0450-4b8a-a8fc-03a055437735
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationPoint::operator=
Assigns ptSrc to CAnimationPoint.  
  
## Syntax  
  
```  
void operator=(  
   const CPoint& ptSrc  
);  
```  
  
#### Parameters  
 `ptSrc`  
 Refers to CPoint or POINT.  
  
## Remarks  
 Assigns ptSrc to CAnimationPoint. It's recommended to do that before animation start, because this operator calls SetDefaultValue, which recreates the underlying COM objects for X and Y coordinates if they have been created. If you subscribed this animation object to events (ValueChanged or IntegerValueChanged), you need to re-enable these events.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationPoint Class](../vs140/CAnimationPoint-Class.md)