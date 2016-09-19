---
title: "CTreeCtrl::GetBkColor"
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
ms.assetid: e042b0b8-77a2-4d54-add4-48927c19b2ec
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::GetBkColor
This member function implements the behavior of the Win32 message [TVM_GETBKCOLOR](http://msdn.microsoft.com/library/windows/desktop/bb773570), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Syntax  
  
```  
  
COLORREF GetBkColor( ) const;  
  
```  
  
## Return Value  
 A **COLORREF** value that represents the current window background color for the control. If this value is -1, the control is using the system window color. In this case, you can use `::GetSysColor(COLOR_WINDOW)` to get the current system color that the control is using.  
  
## Example  
 See the example for [CTreeCtrl::SetTextColor](../vs140/CTreeCtrl--SetTextColor.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::SetBkColor](../vs140/CTreeCtrl--SetBkColor.md)