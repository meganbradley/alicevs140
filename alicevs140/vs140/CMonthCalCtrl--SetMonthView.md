---
title: "CMonthCalCtrl::SetMonthView"
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
ms.assetid: ee8a2f21-d023-4fd0-ad8a-f7b90c4552f2
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMonthCalCtrl::SetMonthView
Sets the current month calendar control to display the month view.  
  
## Syntax  
  
```  
BOOL SetMonthView();  
```  
  
## Return Value  
 `true` if this method is successful; otherwise, `false`.  
  
## Remarks  
 This method uses the [CMonthCalCtrl::SetCurrentView](../vs140/CMonthCalCtrl--SetCurrentView.md) method to set the view to `MCMV_MONTH`, which represents the month view.  
  
## Requirements  
 **Header:** afxdtctl.h  
  
 This control is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## Example  
 The following code example defines the variable, `m_monthCalCtrl`, that is used to programmatically access the month calendar control. This variable is used in the next example.  
  
 [!CODE [NVC_MFC_CMonthCalCtrl_s1#9](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CMonthCalCtrl_s1#9)]  
  
## Example  
 The following code example sets the month calendar control to display the month, year, decade, and century views.  
  
 [!CODE [NVC_MFC_CMonthCalCtrl_s1#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CMonthCalCtrl_s1#2)]  
  
## See Also  
 [CMonthCalCtrl Class](../vs140/CMonthCalCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [MCM_SETCURRENTVIEW](http://msdn.microsoft.com/library/windows/desktop/bb760998)   
 [CMonthCalCtrl::SetCurrentView](../vs140/CMonthCalCtrl--SetCurrentView.md)