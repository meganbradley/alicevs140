---
title: "CMiniFrameWnd::Create"
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
ms.assetid: 9d966ea0-ad49-4f34-adcd-6843664cb7ee
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMiniFrameWnd::Create
Creates the Windows mini-frame window and attaches it to the `CMiniFrameWnd` object.  
  
## Syntax  
  
```  
  
      virtual BOOL Create(  
   LPCTSTR lpClassName,  
   LPCTSTR lpWindowName,  
   DWORD dwStyle,  
   const RECT& rect,  
   CWnd* pParentWnd = NULL,  
   UINT nID = 0  
);  
```  
  
#### Parameters  
 `lpClassName`  
 Points to a null-terminated character string that names the Windows class. The class name can be any name registered with the global [AfxRegisterWndClass](../vs140/AfxRegisterWndClass.md) function. If **NULL**, the window class will be registered for you by the framework. MFC gives the default class the following styles and attributes:  
  
-   Sets style bit **CS_DBLCLKS**, which sends double-click messages to the window procedure when the user double-clicks the mouse.  
  
-   Sets style bits **CS_HREDRAW** and **CS_VREDRAW**, which direct the contents of the client area to be redrawn when the window changes size.  
  
-   Sets the class cursor to the Windows standard **IDC_ARROW**.  
  
-   Sets the class background brush to **NULL**, so the window will not erase its background.  
  
-   Sets the class icon to the standard, waving-flag Windows logo icon.  
  
-   Sets the window to the default size and position, as indicated by Windows.  
  
 `lpWindowName`  
 Points to a null-terminated character string that contains the window name.  
  
 `dwStyle`  
 Specifies the window style attributes. These can include standard window styles and one or more of the following special styles:  
  
-   **MFS_MOVEFRAME** Allows the mini-frame window to be moved by clicking on any edge of the window, not just the caption.  
  
-   **MFS_4THICKFRAME** Disables resizing of the mini-frame window.  
  
-   **MFS_SYNCACTIVE** Synchronizes the activation of the mini-frame window to the activation of its parent window.  
  
-   **MFS_THICKFRAME** Allows the mini-frame window to be sized as small as the contents of the client area allow.  
  
-   **MFS_BLOCKSYSMENU** Disables access to the system menu and the control menu, and converts them to part of the caption (title bar).  
  
 See [CWnd::Create](../vs140/CWnd--Create.md) for a description of possible window style values. The typical combination used for mini-frame windows is **WS_POPUP&#124;WS_CAPTION&#124;WS_SYSMENU**.  
  
 `rect`  
 A `RECT` structure specifying the desired dimensions of the window.  
  
 `pParentWnd`  
 Points to the parent window. Use **NULL** for top-level windows.  
  
 `nID`  
 If the mini-frame window is created as a child window, this is the identifier of the child control; otherwise 0.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 **Create** initializes the window's class name and window name and registers default values for its style and parent.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMiniFrameWnd Class](../vs140/CMiniFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFrameWnd::Create](../vs140/CFrameWnd--Create.md)   
 [CWnd::Create](../vs140/CWnd--Create.md)   
 [CWnd::CreateEx](../vs140/CWnd--CreateEx.md)   
 [CFrameWnd Class](../vs140/CFrameWnd-Class.md)