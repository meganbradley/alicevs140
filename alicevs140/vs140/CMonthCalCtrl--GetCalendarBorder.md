---
title: "CMonthCalCtrl::GetCalendarBorder"
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
ms.assetid: 6d2bdf58-221a-4d88-964e-94d8d52baeec
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMonthCalCtrl::GetCalendarBorder
Retrieves the width of the border of the current month calendar control.  
  
## Syntax  
  
```  
int GetCalendarBorder() const;  
```  
  
## Return Value  
 The width of the control border, in pixels.  
  
## Remarks  
 This method sends the [MCM_GETCALENDARBORDER](http://msdn.microsoft.com/library/windows/desktop/bb760945) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxdtctl.h  
  
 This control is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## See Also  
 [CMonthCalCtrl Class](../vs140/CMonthCalCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [MCM_GETCALENDARBORDER](http://msdn.microsoft.com/library/windows/desktop/bb760945)   
 [CMonthCalCtrl::SetCalendarBorder](../vs140/CMonthCalCtrl--SetCalendarBorder.md)