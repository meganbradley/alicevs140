---
title: "CDateTimeCtrl::SetMonthCalStyle"
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
ms.assetid: 011c4dbc-5743-462a-91b8-ac29aab6270d
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDateTimeCtrl::SetMonthCalStyle
Sets the style of the drop-down month calendar control that is associated with the current date and time picker control.  
  
## Syntax  
  
```  
DWORD SetMonthCalStyle(  
      DWORD dwStyle  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `dwStyle`|A new month calendar control style, which is a bitwise combination (OR) of month calendar control styles. For more information, see [Month Calendar Control Styles](http://msdn.microsoft.com/library/windows/desktop/bb760919).|  
  
## Return Value  
 The previous style of the drop-down month calendar control.  
  
## Remarks  
 This method sends the [DTM_SETMCSTYLE](http://msdn.microsoft.com/library/windows/desktop/bb761778) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 The following code example defines the variable, `m_dateTimeCtrl`, that is used to programmatically access the date and time picker control. This variable is used in the next example.  
  
 [!CODE [NVC_MFC_CDateTimeCtrl_s1#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CDateTimeCtrl_s1#1)]  
  
## Example  
 The following code example sets the date and time picker control to display week numbers, abbreviated names of days of the week, and no today indicator.  
  
 [!CODE [NVC_MFC_CDateTimeCtrl_s1#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CDateTimeCtrl_s1#3)]  
  
## Requirements  
 **Header:** afxdtctl.h  
  
 This method is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
## See Also  
 [CDateTimeCtrl Class](../vs140/CDateTimeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDateTimeCtrl::GetMonthCalStyle](../vs140/CDateTimeCtrl--GetMonthCalStyle.md)   
 [DTM_SETMCSTYLE](http://msdn.microsoft.com/library/windows/desktop/bb761778)   
 [Date and Time Picker Control Styles](http://msdn.microsoft.com/library/windows/desktop/bb761728)