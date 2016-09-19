---
title: "CWnd::OnQueryDragIcon"
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
ms.assetid: 47b18fa3-6a45-4081-9def-b024badafb5a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnQueryDragIcon
The framework calls this member function by a minimized (iconic) window that does not have an icon defined for its class.  
  
## Syntax  
  
```  
  
afx_msg HCURSOR OnQueryDragIcon( );  
```  
  
## Return Value  
 A doubleword value that contains a cursor or icon handle in the low-order word. The cursor or icon must be compatible with the display driver's resolution. If the application returns **NULL**, the system displays the default cursor. The default return value is **NULL**.  
  
## Remarks  
 The system makes this call to obtain the cursor to display while the user drags the minimized window. If an application returns the handle of an icon or cursor, the system converts it to black-and-white. If an application returns a handle, the handle must identify a monochrome cursor or icon compatible with the display driver's resolution. The application can call the [CWinApp::LoadCursor](../vs140/CWinApp--LoadCursor.md) or [CWinApp::LoadIcon](../vs140/CWinApp--LoadIcon.md) member functions to load a cursor or icon from the resources in its executable file and to obtain this handle.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::LoadCursor](../vs140/CWinApp--LoadCursor.md)   
 [CWinApp::LoadIcon](../vs140/CWinApp--LoadIcon.md)   
 [WM_QUERYDRAGICON](http://msdn.microsoft.com/library/windows/desktop/ms632639)