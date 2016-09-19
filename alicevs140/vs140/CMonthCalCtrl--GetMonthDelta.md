---
title: "CMonthCalCtrl::GetMonthDelta"
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
ms.assetid: 45869c05-d301-4b06-835f-c26287874215
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMonthCalCtrl::GetMonthDelta
Retrieves the scroll rate for a month calendar control.  
  
## Syntax  
  
```  
  
int GetMonthDelta( ) const;  
  
```  
  
## Return Value  
 The scroll rate for the month calendar control. The scroll rate is the number of months that the control moves its display when the user clicks a scroll button once.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [MCM_GETMONTHDELTA](http://msdn.microsoft.com/library/windows/desktop/bb760980), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxdtctl.h  
  
## See Also  
 [CMonthCalCtrl Class](../vs140/CMonthCalCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMonthCalCtrl::SetMonthDelta](../vs140/CMonthCalCtrl--SetMonthDelta.md)