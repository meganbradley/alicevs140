---
title: "CMDIFrameWnd::MDIGetActive"
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
ms.assetid: 7f18da52-fcb7-4f5b-8697-826e52e8ca6b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWnd::MDIGetActive
Retrieves the current active MDI child window, along with a flag indicating whether the child window is maximized.  
  
## Syntax  
  
```  
  
      CMDIChildWnd* MDIGetActive(  
   BOOL* pbMaximized = NULL   
) const;  
```  
  
#### Parameters  
 *pbMaximized*  
 A pointer to a **BOOL** return value. Set to **TRUE** on return if the window is maximized; otherwise **FALSE**.  
  
## Return Value  
 A pointer to the active MDI child window.  
  
## Example  
 See the example for [CMDIChildWnd::MDIMaximize](../vs140/CMDIChildWnd--MDIMaximize.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMDIFrameWnd Class](../vs140/CMDIFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMDIFrameWnd::MDIActivate](../vs140/CMDIFrameWnd--MDIActivate.md)   
 [WM_MDIGETACTIVE](http://msdn.microsoft.com/library/windows/desktop/ms644915)