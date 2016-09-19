---
title: "CWnd::SetCapture"
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
ms.assetid: 3bfbc59d-c061-4436-b584-0cef7630f7e2
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::SetCapture
Causes all subsequent mouse input to be sent to the current `CWnd` object regardless of the position of the cursor.  
  
## Syntax  
  
```  
  
CWnd* SetCapture();  
```  
  
## Return Value  
 A pointer to the window object that previously received all mouse input. It is `NULL` if there is no such window. The returned pointer may be temporary and should not be stored for later use.  
  
## Remarks  
 When `CWnd` no longer requires all mouse input, the application should call the [ReleaseCapture](http://msdn.microsoft.com/library/windows/desktop/ms646261) function so that other windows can receive mouse input.  
  
 While mouse input is captured, no `WM_NCHITTEST` or `WM_SETCURSOR` messages are sent to the active window.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [ReleaseCapture](http://msdn.microsoft.com/library/windows/desktop/ms646261)   
 [SetCapture](http://msdn.microsoft.com/library/windows/desktop/ms646262)   
 [CWnd::GetCapture](../vs140/CWnd--GetCapture.md)