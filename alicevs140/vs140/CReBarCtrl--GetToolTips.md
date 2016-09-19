---
title: "CReBarCtrl::GetToolTips"
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
ms.assetid: 8db578cf-6d28-4c5a-824f-513ccb83342a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CReBarCtrl::GetToolTips
Implements the behavior of the Win32 message [RB_GETTOOLTIPS](http://msdn.microsoft.com/library/windows/desktop/bb774477), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Syntax  
  
```  
  
CToolTipCtrl* GetToolTips( ) const;  
  
```  
  
## Return Value  
 A pointer to a [CToolTipCtrl](../vs140/CToolTipCtrl-Class.md) object.  
  
## Remarks  
 Note that the MFC implementation of `GetToolTips` returns a pointer to a `CToolTipCtrl`, rather than an `HWND`.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CReBarCtrl Class](../vs140/CReBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CReBarCtrl::SetToolTips](../vs140/CReBarCtrl--SetToolTips.md)