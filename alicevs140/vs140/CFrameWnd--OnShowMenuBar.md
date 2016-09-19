---
title: "CFrameWnd::OnShowMenuBar"
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
ms.assetid: 914e4d23-e441-4cbd-b378-be6731301cdf
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWnd::OnShowMenuBar
This function is called when the system is about to display the menu bar in the current MFC application.  
  
## Syntax  
  
```  
virtual void OnShowMenuBar();  
```  
  
## Remarks  
 This event handler enables your application to perform custom actions when the menu is about to be displayed. You cannot prevent the menu from being displayed, but you can, for example, call other methods to retrieve the menu style or state.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CFrameWnd Class](../vs140/CFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFrameWnd::OnHideMenuBar](../vs140/CFrameWnd--OnHideMenuBar.md)