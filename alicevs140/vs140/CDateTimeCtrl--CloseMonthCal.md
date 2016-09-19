---
title: "CDateTimeCtrl::CloseMonthCal"
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
ms.assetid: 36bce7ff-0f97-4ed4-a520-6cb81c35e6eb
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDateTimeCtrl::CloseMonthCal
Closes the current date and time picker control.  
  
## Syntax  
  
```  
void CloseMonthCal() const;  
```  
  
## Remarks  
 This method sends the [DTM_CLOSEMONTHCAL](http://msdn.microsoft.com/library/windows/desktop/bb761753) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 The following code example defines the variable, `m_dateTimeCtrl`, that is used to programmatically access the date and time picker control. This variable is used in the next example.  
  
 [!CODE [NVC_MFC_CDateTimeCtrl_s1#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CDateTimeCtrl_s1#1)]  
  
## Example  
 The following code example closes the drop-down calendar for the current date and time picker control.  
  
 [!CODE [NVC_MFC_CDateTimeCtrl_s1#5](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CDateTimeCtrl_s1#5)]  
  
## Requirements  
 **Header:** afxdtctl.h  
  
 This method is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
## See Also  
 [CDateTimeCtrl Class](../vs140/CDateTimeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [DTM_CLOSEMONTHCAL](http://msdn.microsoft.com/library/windows/desktop/bb761753)