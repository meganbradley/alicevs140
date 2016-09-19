---
title: "CMonthCalCtrl::HitTest"
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
ms.assetid: 7bbefc19-18b2-4be1-baaa-59515680d697
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMonthCalCtrl::HitTest
Determines which month calendar control, if any, is at a specified position.  
  
## Syntax  
  
```  
  
      DWORD HitTest(  
   PMCHITTESTINFO pMCHitTest   
);  
```  
  
#### Parameters  
 *pMCHitTest*  
 A pointer to a [MCHITTESTINFO](http://msdn.microsoft.com/library/windows/desktop/bb760927) structure containing hit testing points for the month calendar control.  
  
## Return Value  
 A `DWORD` value. Equal to the **uHit** member of the **MCHITTESTINFO** structure.  
  
## Remarks  
 `HitTest` uses the **MCHITTESTINFO** structure, which contains information about the hit test.  
  
## Requirements  
 **Header:** afxdtctl.h  
  
## See Also  
 [CMonthCalCtrl Class](../vs140/CMonthCalCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)