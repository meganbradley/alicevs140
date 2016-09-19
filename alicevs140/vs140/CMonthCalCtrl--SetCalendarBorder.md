---
title: "CMonthCalCtrl::SetCalendarBorder"
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
ms.assetid: 7d8395ff-a7e4-487f-ae1a-3d626dc2ecf8
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMonthCalCtrl::SetCalendarBorder
Sets the width of the border of the current month calendar control.  
  
## Syntax  
  
```  
void SetCalendarBorder(  
     int cxyBorder  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `cxyBorder`|The width of the border, in pixels.|  
  
## Remarks  
 If this method succeeds, the border width is set to the `cxyBorder` parameter. Otherwise, the border width is reset to the default value that is specified by the current [theme](_inet_themes_visualstyles_overview), or zero if themes are not used.  
  
 This method sends the [MCM_SETCALENDARBORDER](http://msdn.microsoft.com/library/windows/desktop/bb760993) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxdtctl.h  
  
 This control is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## Example  
 The following code example defines the variable, `m_monthCalCtrl`, that is used to programmatically access the month calendar control. This variable is used in the next example.  
  
 [!CODE [NVC_MFC_CMonthCalCtrl_s1#9](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CMonthCalCtrl_s1#9)]  
  
## Example  
 The following code example sets the border width of the month calendar control to eight pixels. Use the [CMonthCalCtrl::GetCalendarBorder](../vs140/CMonthCalCtrl--GetCalendarBorder.md) method to determine whether this method succeeded.  
  
 [!CODE [NVC_MFC_CMonthCalCtrl_s1#6](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CMonthCalCtrl_s1#6)]  
  
## See Also  
 [CMonthCalCtrl Class](../vs140/CMonthCalCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMonthCalCtrl::SetCalendarBorderDefault](../vs140/CMonthCalCtrl--SetCalendarBorderDefault.md)   
 [MCM_SETCALENDARBORDER](http://msdn.microsoft.com/library/windows/desktop/bb760993)   
 [Themes and Visual Styles](_inet_themes_visualstyles_overview)