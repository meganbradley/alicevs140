---
title: "CWnd::OnContextMenu"
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
ms.assetid: 0fa9df29-0c6f-411b-af7f-fac7a1af337e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnContextMenu
Called by the framework when the user has clicked the right mouse button (right clicked) in the window.  
  
## Syntax  
  
```  
  
      afx_msg void OnContextMenu(  
   CWnd* pWnd,  
   CPoint pos   
);  
```  
  
#### Parameters  
 `pWnd`  
 Handle to the window in which the user right clicked the mouse. This can be a child window of the window receiving the message. For more information about processing this message, see the Remarks section.  
  
 `pos`  
 Position of the cursor, in screen coordinates, at the time of the mouse click.  
  
## Remarks  
 You can process this message by displaying a context menu using the [TrackPopupMenu](../vs140/CMenu--TrackPopupMenu.md).  
  
 If you do not display a context menu you should pass this message onto the [DefWindowProc](../vs140/CWnd--DefWindowProc.md) function. If your window is a child window, `DefWindowProc` sends the message to the parent. Otherwise, `DefWindowProc` displays a default context menu if the specified position is in the window's caption.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)