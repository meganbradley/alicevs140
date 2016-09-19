---
title: "CMiniFrameWnd::CreateEx"
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
ms.assetid: 4fab5e28-61f8-484b-9f61-0f91a5443c57
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMiniFrameWnd::CreateEx
Creates a `CMiniFrameWnd` object.  
  
## Syntax  
  
```  
  
      virtual BOOL CreateEx(   
   DWORD dwExStyle,   
   LPCTSTR lpClassName,    
   LPCTSTR lpWindowName,   
   DWORD dwStyle,    
   const RECT& rect,   
   CWnd* pParentWnd = NULL,    
   UINT nID = 0   
);  
```  
  
#### Parameters  
 `dwExStyle`  
 Specifies the extended style of the `CMiniFrameWnd` being created. Apply any of the [extended window styles](../vs140/Extended-Window-Styles.md) to the window.  
  
 `lpClassName`  
 Points to a null-terminated character string that names the Windows class (a [WNDCLASS](http://msdn.microsoft.com/library/windows/desktop/ms633576) structure). The class name can be any name registered with the global [AfxRegisterWndClass](../vs140/AfxRegisterWndClass.md) function or any of the predefined control-class names. It must not be **NULL**.  
  
 `lpWindowName`  
 Points to a null-terminated character string that contains the window name.  
  
 `dwStyle`  
 Specifies the window style attributes. See [Window Styles](../vs140/Window-Styles.md) and [CWnd::Create](../vs140/CWnd--Create.md) for a description of the possible values.  
  
 `rect`  
 The size and position of the window, in client coordinates of `pParentWnd`.  
  
 `pParentWnd`  
 Points to the parent window object.  
  
 `nID`  
 The identifier of the child window.  
  
## Return Value  
 Returns TRUE on success, FALSE on failure.  
  
## Remarks  
 The `CreateEx` parameters specify the **WNDCLASS**, window style, and (optionally) initial position and size of the window. `CreateEx` also specifies the window's parent (if any) and ID.  
  
 When `CreateEx` executes, Windows sends the [WM_GETMINMAXINFO](../vs140/CWnd--OnGetMinMaxInfo.md), [WM_NCCREATE](../vs140/CWnd--OnNcCreate.md), [WM_NCCALCSIZE](../vs140/CWnd--OnNcCalcSize.md), and [WM_CREATE](../vs140/CWnd--OnCreate.md) messages to the window.  
  
 To extend the default message handling, derive a class from `CMiniFrameWnd`, add a message map to the new class, and provide member functions for the above messages. Override `OnCreate`, for example, to perform needed initialization for a new class.  
  
 Override further **On***Message* message handlers to add further functionality to your derived class.  
  
 If the **WS_VISIBLE** style is given, Windows sends the window all the messages required to activate and show the window. If the window style specifies a title bar, the window title pointed to by the `lpszWindowName` parameter is displayed in the title bar.  
  
 The `dwStyle` parameter can be any combination of [window styles](../vs140/Window-Styles.md).  
  
 The old style Palette toolbox windows are no longer supported. The old style, which did not have an "X" Close button, was supported when running an MFC application on previous versions of Windows, but is no longer supported in Visual C++.NET. Only the new `WS_EX_TOOLWINDOW` style is now supported; for a description of this style, see [Extended Window Styles](../vs140/Extended-Window-Styles.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMiniFrameWnd Class](../vs140/CMiniFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFrameWnd::Create](../vs140/CFrameWnd--Create.md)   
 [CWnd::Create](../vs140/CWnd--Create.md)   
 [CWnd::CreateEx](../vs140/CWnd--CreateEx.md)   
 [CFrameWnd Class](../vs140/CFrameWnd-Class.md)