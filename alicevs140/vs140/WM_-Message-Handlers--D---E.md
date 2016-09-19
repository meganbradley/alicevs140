---
title: "WM_ Message Handlers: D - E"
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
ms.topic: article
ms.assetid: 56fb89c8-68a8-4adf-883e-a9f63bf677e9
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# WM_ Message Handlers: D - E
The following map entries on the left correspond to the function prototypes on the right:  
  
|Map entry|Function prototype|  
|---------------|------------------------|  
|ON_WM_DEADCHAR()|afx_msg void [OnDeadChar](../vs140/CWnd--OnDeadChar.md)(UINT, UINT, UINT);|  
|ON_WM_DELETEITEM()|afx_msg void [OnDeleteItem](../vs140/CWnd--OnDeleteItem.md)(LPDELETEITEMSTRUCT);|  
|ON_WM_DESTROY()|afx_msg void [OnDestroy](../vs140/CWnd--OnDestroy.md)();|  
|ON_WM_DESTROYCLIPBOARD()|afx_msg void [OnDestroyClipboard](../vs140/CWnd--OnDestroyClipboard.md)();|  
|ON_WM_DEVICECHANGE()|afx_msg void [OnDeviceChange](../vs140/CWnd--OnDeviceChange.md)(UINT, DWORD);|  
|ON_WM_DEVMODECHANGE()|afx_msg void [OnDevModeChange](../vs140/CWnd--OnDevModeChange.md)(LPSTR);|  
|ON_WM_DRAWCLIPBOARD()|afx_msg void [OnDrawClipboard](../vs140/CWnd--OnDrawClipboard.md)();|  
|ON_WM_DRAWITEM()|afx_msg void [OnDrawItem](../vs140/CWnd--OnDrawItem.md)(LPDRAWITEMSTRUCT);|  
|ON_WM_DROPFILES()|afx_msg void [OnDropFiles](../vs140/CWnd--OnDropFiles.md)(HDROP);|  
|ON_WM_DWMCOLORIZATIONCOLORCHANGED()|afx_msg void [OnColorizationColorChanged](../vs140/CWnd--OnColorizationColorChanged.md)(DWORD, BOOL);|  
|ON_WM_DWMCOMPOSITIONCHANGED()|afx_msg void [OnCompositionChanged](../vs140/CWnd--OnCompositionChanged.md)();|  
|ON_WM_DWMNCRENDERINGCHANGED()|afx_msg void [OnNcRenderingChanged](../vs140/CWnd--OnNcRenderingChanged.md)(BOOL);|  
|ON_WM_DWMWINDOWMAXIMIZEDCHANGE()|afx_msg void [OnWindowMaximizedChanged](../vs140/CWnd--OnWindowMaximizedChanged.md)(BOOL);|  
|ON_WM_ENABLE()|afx_msg void [OnEnable](../vs140/CWnd--OnEnable.md)(BOOL);|  
|ON_WM_ENDSESSION()|afx_msg void [OnEndSession](../vs140/CWnd--OnEndSession.md)(BOOL);|  
|ON_WM_ENTERIDLE()|afx_msg void [OnEnterIdle](../vs140/CWnd--OnEnterIdle.md)(UINT, CWnd*);|  
|ON_WM_ENTERSIZEMOVE()|afx_msg void [OnEnterSizeMove](../vs140/CWnd--OnEnterSizeMove.md)();|  
|ON_WM_ERASEBKGND()|afx_msg BOOL [OnEraseBkgnd](../vs140/CWnd--OnEraseBkgnd.md)(CDC*);|  
|ON_WM_EXITSIZEMOVE()|afx_msg void [OnExitSizeMove](../vs140/CWnd--OnExitSizeMove.md)();|  
  
## See Also  
 [Message Maps](../vs140/Message-Maps--MFC-.md)   
 [Handlers for WM_ Messages](../vs140/Handlers-for-WM_-Messages.md)