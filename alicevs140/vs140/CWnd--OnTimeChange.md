---
title: "CWnd::OnTimeChange"
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
ms.assetid: e09a0c2a-bcb1-48ae-9bf6-47ad12c5174f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnTimeChange
The framework calls this member function after the system time is changed.  
  
## Syntax  
  
```  
  
afx_msg void OnTimeChange( );  
```  
  
## Remarks  
 Have any application that changes the system time send this message to all top-level windows. To send the `WM_TIMECHANGE` message to all top-level windows, an application can use the [SendMessage](http://msdn.microsoft.com/library/windows/desktop/ms644950) Windows function with its *hwnd* parameter set to **HWND_BROADCAST**.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [SendMessage](http://msdn.microsoft.com/library/windows/desktop/ms644950)   
 [WM_TIMECHANGE](http://msdn.microsoft.com/library/windows/desktop/ms725498)