---
title: "CWnd::OnPaint"
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
ms.assetid: eb3b1ad8-2183-42ca-a0e6-64d8667a88c8
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnPaint
The framework calls this member function when Windows or an application makes a request to repaint a portion of an application's window.  
  
## Syntax  
  
```  
  
afx_msg void OnPaint( );  
```  
  
## Remarks  
 The [WM_PAINT](http://msdn.microsoft.com/library/windows/desktop/dd145137) message is sent when the [UpdateWindow](../vs140/CWnd--UpdateWindow.md) or [RedrawWindow](../vs140/CWnd--RedrawWindow.md) member function is called.  
  
 A window may receive internal paint messages as a result of calling the `RedrawWindow` member function with the **RDW_INTERNALPAINT** flag set. In this case, the window may not have an update region. An application should call the [GetUpdateRect](../vs140/CWnd--GetUpdateRect.md) member function to determine whether the window has an update region. If `GetUpdateRect` returns 0, the application should not call the [BeginPaint](../vs140/CWnd--BeginPaint.md) and [EndPaint](../vs140/CWnd--EndPaint.md) member functions.  
  
 It is an application's responsibility to check for any necessary internal repainting or updating by looking at its internal data structures for each `WM_PAINT` message because a `WM_PAINT` message may have been caused by both an invalid area and a call to the `RedrawWindow` member function with the **RDW_INTERNALPAINT** flag set.  
  
 An internal `WM_PAINT` message is sent only once by Windows. After an internal `WM_PAINT` message is sent to a window by the `UpdateWindow` member function, no further `WM_PAINT` messages will be sent or posted until the window is invalidated or until the `RedrawWindow` member function is called again with the **RDW_INTERNALPAINT** flag set.  
  
 For information on rendering an image in document/view applications, see [CView::OnDraw](../vs140/CView--OnDraw.md).  
  
 For more information about using **WM_Paint**, see the following topics in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]:  
  
-   [The WM_PAINT Message](http://msdn.microsoft.com/library/windows/desktop/dd145137)  
  
-   [Using the WM_PAINT Message](http://msdn.microsoft.com/library/windows/desktop/dd145193)  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::BeginPaint](../vs140/CWnd--BeginPaint.md)   
 [CWnd::EndPaint](../vs140/CWnd--EndPaint.md)   
 [CWnd::RedrawWindow](../vs140/CWnd--RedrawWindow.md)   
 [CPaintDC Class](../vs140/CPaintDC-Class.md)   
 [CView::OnDraw](../vs140/CView--OnDraw.md)