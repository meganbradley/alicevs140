---
title: "CWnd::OnCancelMode"
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
ms.assetid: c2686960-7fa5-4ebc-af39-e76e8253a1fe
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnCancelMode
The framework calls this member function to inform `CWnd` to cancel any internal mode.  
  
## Syntax  
  
```  
  
afx_msg void OnCancelMode( );  
```  
  
## Remarks  
 If the `CWnd` object has the focus, its `OnCancelMode` member function is called when a dialog box or message box is displayed. This gives the `CWnd` the opportunity to cancel modes such as mouse capture.  
  
 The default implementation responds by calling the [ReleaseCapture](http://msdn.microsoft.com/library/windows/desktop/ms646261) Windows function. Override this member function in your derived class to handle other modes.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::Default](../vs140/CWnd--Default.md)   
 [ReleaseCapture](http://msdn.microsoft.com/library/windows/desktop/ms646261)   
 [WM_CANCELMODE](http://msdn.microsoft.com/library/windows/desktop/ms632615)