---
title: "CMonthCalCtrl::GetCalendarGridInfo"
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
ms.assetid: da8978f5-e939-45cd-8620-e6042690a071
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMonthCalCtrl::GetCalendarGridInfo
Retrieves information about the current month calendar control.  
  
## Syntax  
  
```  
BOOL GetCalendarGridInfo(  
     PMCGRIDINFO pmcGridInfo  
) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[out] `pmcGridInfo`|Pointer to a [MCGRIDINFO](http://msdn.microsoft.com/library/windows/desktop/bb760925) structure that receives information about the current month calendar control. The caller is responsible for allocating and initializing this structure.|  
  
## Return Value  
 `true` if this method is successful; otherwise, `false`.  
  
## Remarks  
 This method sends the [MCM_GETCALENDARGRIDINFO](http://msdn.microsoft.com/library/windows/desktop/bb760949) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxdtctl.h  
  
 This control is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## Example  
 The following code example defines the variable, `m_monthCalCtrl`, that is used to programmatically access the month calendar control. This variable is used in the next example.  
  
 [!CODE [NVC_MFC_CMonthCalCtrl_s1#9](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CMonthCalCtrl_s1#9)]  
  
## Example  
 The following code example uses the `GetCalendarGridInfo` method to retrieve the calendar date that the current month calendar control displays.  
  
 [!CODE [NVC_MFC_CMonthCalCtrl_s1#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CMonthCalCtrl_s1#3)]  
  
## See Also  
 [CMonthCalCtrl Class](../vs140/CMonthCalCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [MCM_GETCALENDARGRIDINFO](http://msdn.microsoft.com/library/windows/desktop/bb760949)   
 [MCGRIDINFO](http://msdn.microsoft.com/library/windows/desktop/bb760925)