---
title: "CDateTimeCtrl::GetIdealSize"
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
ms.assetid: d73a6e66-67c2-4c13-a61e-d6627245e60e
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDateTimeCtrl::GetIdealSize
Returns the ideal size of the date and time picker control that is required to display the current date or time.  
  
## Syntax  
  
```  
BOOL GetIdealSize(  
     LPSIZE psize  
) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[out] `psize`|Pointer to a [SIZE](http://msdn.microsoft.com/library/windows/desktop/dd145106) structure that contains the ideal size for the control.|  
  
## Return Value  
 The return value is always `true`.  
  
## Remarks  
 This method sends the [DTM_GETIDEALSIZE](http://msdn.microsoft.com/library/windows/desktop/bb761757) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxdtctl.h  
  
 This method is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
## Example  
 The following code example defines the variable, `m_dateTimeCtrl`, that is used to programmatically access the date and time picker control. This variable is used in the next example.  
  
 [!CODE [NVC_MFC_CDateTimeCtrl_s1#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CDateTimeCtrl_s1#1)]  
  
## Example  
 The following code example retrieves the ideal size to display the date and time picker control.  
  
 [!CODE [NVC_MFC_CDateTimeCtrl_s1#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CDateTimeCtrl_s1#2)]  
  
## See Also  
 [CDateTimeCtrl Class](../vs140/CDateTimeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [DTM_GETIDEALSIZE](http://msdn.microsoft.com/library/windows/desktop/bb761757)   
 [SIZE](http://msdn.microsoft.com/library/windows/desktop/dd145106)