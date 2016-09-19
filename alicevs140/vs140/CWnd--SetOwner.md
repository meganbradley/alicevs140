---
title: "CWnd::SetOwner"
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
ms.assetid: c15bc442-1957-4f12-bde1-9f07dabe18b9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::SetOwner
Sets the current window's owner to the specified window object.  
  
## Syntax  
  
```  
  
      void SetOwner(  
   CWnd* pOwnerWnd   
);  
```  
  
#### Parameters  
 *pOwnerWnd*  
 Identifies the new owner of the window object. If this parameter is **NULL**, the window object has no owner.  
  
## Remarks  
 This owner can then receive command messages from the current window object. By default, the parent of the current window is its owner.  
  
 It is often useful to establish connections between window objects that are unrelated to the window hierarchy. For example, [CToolBar](../vs140/CToolBar-Class.md) sends notifications to its owner instead of to its parent. This allows the toolbar to become the child of one window (such as an OLE container application window) while sending notifications to another window (such as the in-place frame window). Furthermore, when a server window is deactivated or activated during in-place editing, any window owned by the frame window is hidden or shown. This ownership is explicitly set with a call to `SetOwner`.  
  
 The ownership concept of this function is different from the ownership concept of [GetWindow](http://msdn.microsoft.com/library/windows/desktop/ms633515).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::GetOwner](../vs140/CWnd--GetOwner.md)   
 [CToolBar Class](../vs140/CToolBar-Class.md)