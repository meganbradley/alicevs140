---
title: "CMonthCalCtrl::SetCalendarBorderDefault"
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
ms.assetid: 5f7f7248-80d0-426d-b4c8-763a6e58a1bc
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMonthCalCtrl::SetCalendarBorderDefault
Sets the default width of the border of the current month calendar control.  
  
## Syntax  
  
```  
void SetCalendarBorderDefault();  
```  
  
## Remarks  
 The border width is set to the default value specified by the current [theme](_inet_themes_visualstyles_overview), or zero if themes are not used.  
  
 This method sends the [MCM_SETCALENDARBORDER](http://msdn.microsoft.com/library/windows/desktop/bb760993) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxdtctl.h  
  
 This control is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## See Also  
 [CMonthCalCtrl Class](../vs140/CMonthCalCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMonthCalCtrl::SetCalendarBorder](../vs140/CMonthCalCtrl--SetCalendarBorder.md)   
 [MCM_SETCALENDARBORDER](http://msdn.microsoft.com/library/windows/desktop/bb760993)   
 [Themes and Visual Styles](_inet_themes_visualstyles_overview)