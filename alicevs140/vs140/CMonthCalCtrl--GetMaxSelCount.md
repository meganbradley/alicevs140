---
title: "CMonthCalCtrl::GetMaxSelCount"
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
ms.assetid: e705dfcd-94c4-473a-96f5-63e97ad86fd5
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMonthCalCtrl::GetMaxSelCount
Retrieves the current maximum number of days that can be selected in a month calendar control.  
  
## Syntax  
  
```  
  
int GetMaxSelCount( ) const;  
  
```  
  
## Return Value  
 An integer value that represents the total number of days that can be selected for the control.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [MCM_GETMAXSELCOUNT](http://msdn.microsoft.com/library/windows/desktop/bb760960), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. Use this member function for controls with the **MCS_MULTISELECT** style set.  
  
## Example  
 See the example for [CMonthCalCtrl::SetMaxSelCount](../vs140/CMonthCalCtrl--SetMaxSelCount.md).  
  
## Requirements  
 **Header:** afxdtctl.h  
  
## See Also  
 [CMonthCalCtrl Class](../vs140/CMonthCalCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMonthCalCtrl::SetMaxSelCount](../vs140/CMonthCalCtrl--SetMaxSelCount.md)