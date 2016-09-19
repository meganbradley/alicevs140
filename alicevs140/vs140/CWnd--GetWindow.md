---
title: "CWnd::GetWindow"
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
ms.assetid: 383982f3-3687-466b-a849-3b77a7245e1f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::GetWindow
Returns a pointer to the window requested, or **NULL** if none.  
  
## Syntax  
  
```  
CWnd* GetWindow(  
   UINT nCmd   
) const;  
```  
  
#### Parameters  
 `nCmd`  
 Specifies the relationship between `CWnd` and the returned window. It can take one of the following values:  
  
-   **GW_CHILD** Identifies the `CWnd` first child window.  
  
-   **GW_HWNDFIRST** If `CWnd` is a child window, returns the first sibling window. Otherwise, it returns the first top-level window in the list.  
  
-   **GW_HWNDLAST** If `CWnd` is a child window, returns the last sibling window. Otherwise, it returns the last top-level window in the list.  
  
-   **GW_HWNDNEXT** Returns the next window on the window manager's list.  
  
-   **GW_HWNDPREV** Returns the previous window on the window manager's list.  
  
-   **GW_OWNER** Identifies the `CWnd` owner.  
  
## Return Value  
 The returned pointer may be temporary and should not be stored for later use.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::GetParent](../vs140/CWnd--GetParent.md)   
 [CWnd::GetNextWindow](../vs140/CWnd--GetNextWindow.md)   
 [GetWindow](http://msdn.microsoft.com/library/windows/desktop/ms633515)