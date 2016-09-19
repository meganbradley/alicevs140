---
title: "CMDIFrameWnd::MDIMaximize"
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
ms.assetid: eed8c58f-ea2b-4a45-9057-92df2659265b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWnd::MDIMaximize
Maximizes the specified MDI child window.  
  
## Syntax  
  
```  
  
      void MDIMaximize(  
   CWnd* pWnd   
);  
```  
  
#### Parameters  
 `pWnd`  
 Points to the window to maximize.  
  
## Remarks  
 When a child window is maximized, Windows resizes it to make its client area fill the client window. Windows places the child window's Control menu in the frame's menu bar so the user can restore or close the child window. It also adds the title of the child window to the frame-window title.  
  
 If another MDI child window is activated when the currently active MDI child window is maximized, Windows restores the currently active child and maximizes the newly activated child window.  
  
## Example  
 See the example for [CMDIChildWnd::MDIMaximize](../vs140/CMDIChildWnd--MDIMaximize.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMDIFrameWnd Class](../vs140/CMDIFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [WM_MDIMAXIMIZE](http://msdn.microsoft.com/library/windows/desktop/ms644917)   
 [CMDIFrameWnd::MDIRestore](../vs140/CMDIFrameWnd--MDIRestore.md)