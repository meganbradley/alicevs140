---
title: "CMonthCalCtrl::SetCalID"
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
ms.assetid: 9d629550-eb11-4f54-a7e6-bf650b96a763
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMonthCalCtrl::SetCalID
Sets the calendar identifier for the current month calendar control.  
  
## Syntax  
  
```  
BOOL SetCalID(  
     CALID calid  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `calid`|One of the [calendar identifier](http://msdn.microsoft.com/library/windows/desktop/dd317732) constants.|  
  
## Return Value  
 `true` if this method is successful; otherwise, `false`.  
  
## Remarks  
 A calendar identifier specifies a region-specific calendar, such as the Gregorian (localized), Japanese, or Hijri calendars. Use the `SetCalID` method to display a calendar that is specified by the `calid` parameter if the locale that contains the calendar is installed on your computer.  
  
 This method sends the [MCM_SETCALID](http://msdn.microsoft.com/library/windows/desktop/bb760995) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxdtctl.h  
  
 This control is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## Example  
 The following code example defines the variable, `m_monthCalCtrl`, that is used to programmatically access the month calendar control. This variable is used in the next example.  
  
 [!CODE [NVC_MFC_CMonthCalCtrl_s1#9](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CMonthCalCtrl_s1#9)]  
  
## Example  
 The following code example sets the month calendar control to display the Japanese Emperor Era calendar. The `SetCalID` method succeeds only if that calendar is installed on your computer.  
  
 [!CODE [NVC_MFC_CMonthCalCtrl_s1#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CMonthCalCtrl_s1#4)]  
  
## See Also  
 [CMonthCalCtrl Class](../vs140/CMonthCalCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [MCM_SETCALID](http://msdn.microsoft.com/library/windows/desktop/bb760995)   
 [Calendar Identifiers](http://msdn.microsoft.com/library/windows/desktop/dd317732)   
 [CMonthCalCtrl::GetCalID](../vs140/CMonthCalCtrl--GetCalID.md)