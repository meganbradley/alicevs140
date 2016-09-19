---
title: "CMonthCalCtrl::SetCurrentView"
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
ms.assetid: e0a14f18-fbb7-4225-8fd6-f75ffaf1aeca
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMonthCalCtrl::SetCurrentView
Sets the current month calendar control to display the specified view.  
  
## Syntax  
  
```  
BOOL SetCurrentView(  
     DWORD dwNewView  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `dwNewView`|One of the following values that specifies a monthly, annual, decade, or century view.<br /><br /> MCMV_MONTH: Monthly view<br /><br /> MCMV_YEAR: Annual view<br /><br /> MCMV_DECADE: Decade view<br /><br /> MCMV_CENTURY: Century view|  
  
## Return Value  
 `true` if this method is successful; otherwise, `false`.  
  
## Remarks  
 This method sends the [MCM_SETCURRENTVIEW](http://msdn.microsoft.com/library/windows/desktop/bb760998) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxdtctl.h  
  
 This control is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## See Also  
 [CMonthCalCtrl Class](../vs140/CMonthCalCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [MCM_SETCURRENTVIEW](http://msdn.microsoft.com/library/windows/desktop/bb760998)   
 [CMonthCalCtrl::GetCurrentView](../vs140/CMonthCalCtrl--GetCurrentView.md)