---
title: "CDateTimeCtrl::GetMonthCalStyle"
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
ms.assetid: 8ee24ab1-e844-44b1-a8fc-8572845018f6
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDateTimeCtrl::GetMonthCalStyle
Gets the style of the drop-down month calendar control that is associated with the current date and time picker control.  
  
## Syntax  
  
```  
DWORD GetMonthCalStyle() const;  
```  
  
## Return Value  
 The style of the drop-down month calendar control, which is a bitwise combination (OR) of date and time picker control styles. For more information, see [Month Calendar Control Styles](http://msdn.microsoft.com/library/windows/desktop/bb760919).  
  
## Remarks  
 This method sends the [DTM_GETMCSTYLE](http://msdn.microsoft.com/library/windows/desktop/bb761763) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxdtctl.h  
  
 This method is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
## See Also  
 [CDateTimeCtrl Class](../vs140/CDateTimeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDateTimeCtrl::SetMonthCalStyle](../vs140/CDateTimeCtrl--SetMonthCalStyle.md)   
 [DTM_GETMCSTYLE](http://msdn.microsoft.com/library/windows/desktop/bb761763)   
 [Date and Time Picker Control Styles](http://msdn.microsoft.com/library/windows/desktop/bb761728)