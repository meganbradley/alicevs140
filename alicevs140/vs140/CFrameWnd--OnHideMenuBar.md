---
title: "CFrameWnd::OnHideMenuBar"
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
ms.assetid: c87cf2dd-0e80-4d0c-849e-ca763c545019
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWnd::OnHideMenuBar
This function is called when the system is about to hide the menu bar in the current MFC application.  
  
## Syntax  
  
```  
virtual void OnHideMenuBar();  
```  
  
## Remarks  
 This event handler enables your application to perform custom actions when the system is about to hide the menu. You cannot prevent the menu from being hidden, but you can, for example, call other methods to retrieve the menu style or state.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CFrameWnd Class](../vs140/CFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFrameWnd::OnShowMenuBar](../vs140/CFrameWnd--OnShowMenuBar.md)