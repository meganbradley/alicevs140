---
title: "CMonthCalCtrl::GetCurrentView"
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
ms.assetid: a7a24bbf-a24d-48e7-9a13-31859472e4ff
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMonthCalCtrl::GetCurrentView
Retrieves the view that is currently displayed by the current month calendar control.  
  
## Syntax  
  
```  
DWORD GetCurrentView() const;  
```  
  
## Return Value  
 The current view, which is indicated by one of the following values:  
  
|Value|Meaning|  
|-----------|-------------|  
|`MCMV_MONTH`|Monthly view|  
|`MCMV_YEAR`|Annual view|  
|`MCMV_DECADE`|Decade view|  
|`MCMV_CENTURY`|Century view|  
  
## Remarks  
 This method sends the [MCM_GETCURRENTVIEW](http://msdn.microsoft.com/library/windows/desktop/bb760955) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxdtctl.h  
  
 This control is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## Example  
 The following code example defines the variable, `m_monthCalCtrl`, that is used to programmatically access the month calendar control. This variable is used in the next example.  
  
 [!CODE [NVC_MFC_CMonthCalCtrl_s1#9](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CMonthCalCtrl_s1#9)]  
  
## Example  
 The following code example reports which view the month calendar control currently displays.  
  
 [!CODE [NVC_MFC_CMonthCalCtrl_s1#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CMonthCalCtrl_s1#7)]  
  
## See Also  
 [CMonthCalCtrl Class](../vs140/CMonthCalCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [MCM_GETCURRENTVIEW](http://msdn.microsoft.com/library/windows/desktop/bb760955)   
 [CMonthCalCtrl::SetCurrentView](../vs140/CMonthCalCtrl--SetCurrentView.md)