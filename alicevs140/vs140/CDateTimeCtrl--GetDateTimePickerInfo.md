---
title: "CDateTimeCtrl::GetDateTimePickerInfo"
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
ms.assetid: effe8791-f4e8-4499-90b8-e96b8c8ad691
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDateTimeCtrl::GetDateTimePickerInfo
Retrieves information about the current date and time picker control.  
  
## Syntax  
  
```  
BOOL GetDateTimePickerInfo(  
     LPDATETIMEPICKERINFO pDateTimePickerInfo  
) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[out] `pDateTimePickerInfo`|A pointer to a [DATETIMEPICKERINFO](http://msdn.microsoft.com/library/windows/desktop/bb761729) structure that receives a description of the current date and time picker control.<br /><br /> The caller is responsible for allocating this structure. However, this method initializes the `cbSize` member of the structure.|  
  
## Return Value  
 `true` if this method is successful; otherwise, `false`.  
  
## Remarks  
 This method sends the [DTM_GETDATETIMEPICKERINFO](http://msdn.microsoft.com/library/windows/desktop/bb761755) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 The following code example defines the variable, `m_dateTimeCtrl`, that is used to programmatically access the date and time picker control. This variable is used in the next example.  
  
 [!CODE [NVC_MFC_CDateTimeCtrl_s1#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CDateTimeCtrl_s1#1)]  
  
## Example  
 The following code example indicates whether it successfully retrieves information about the current date and time picker control.  
  
 [!CODE [NVC_MFC_CDateTimeCtrl_s1#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CDateTimeCtrl_s1#4)]  
  
## Requirements  
 **Header:** afxdtctl.h  
  
 This method is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
## See Also  
 [CDateTimeCtrl Class](../vs140/CDateTimeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [DTM_GETDATETIMEPICKERINFO](http://msdn.microsoft.com/library/windows/desktop/bb761755)   
 [DATETIMEPICKERINFO](http://msdn.microsoft.com/library/windows/desktop/bb761729)