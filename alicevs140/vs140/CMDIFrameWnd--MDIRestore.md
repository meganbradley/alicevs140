---
title: "CMDIFrameWnd::MDIRestore"
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
ms.assetid: 904b8200-c9d8-4628-9964-e46956adb2d3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWnd::MDIRestore
Restores an MDI child window from maximized or minimized size.  
  
## Syntax  
  
```  
  
      void MDIRestore(  
   CWnd* pWnd   
);  
```  
  
#### Parameters  
 `pWnd`  
 Points to the window to restore.  
  
## Example  
 See the example for [CMDIChildWnd::MDIRestore](../vs140/CMDIChildWnd--MDIRestore.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMDIFrameWnd Class](../vs140/CMDIFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMDIFrameWnd::MDIMaximize](../vs140/CMDIFrameWnd--MDIMaximize.md)   
 [WM_MDIRESTORE](http://msdn.microsoft.com/library/windows/desktop/ms644920)