---
title: "CWnd::SetClipboardViewer"
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
ms.assetid: 57ad2adb-b091-49e1-be58-b53ebd1b28a0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::SetClipboardViewer
Adds this window to the chain of windows that are notified (by means of the `WM_DRAWCLIPBOARD` message) whenever the content of the Clipboard is changed.  
  
## Syntax  
  
```  
  
HWND SetClipboardViewer( );  
```  
  
## Return Value  
 A handle to the next window in the Clipboard-viewer chain if successful. Applications should save this handle (it can be stored as a member variable) and use it when responding to Clipboard-viewer chain messages.  
  
## Remarks  
 A window that is part of the Clipboard-viewer chain must respond to [WM_DRAWCLIPBOARD](../vs140/CWnd--OnDrawClipboard.md), [WM_CHANGECBCHAIN](../vs140/CWnd--OnChangeCbChain.md), and [WM_DESTROY](../vs140/CWnd--OnDestroy.md) messages and pass the message to the next window in the chain.  
  
 This member function sends a `WM_DRAWCLIPBOARD` message to the window. Since the handle to the next window in the Clipboard-viewer chain has not yet been returned, the application should not pass on the `WM_DRAWCLIPBOARD` message that it receives during the call to `SetClipboardViewer`.  
  
 To remove itself from the Clipboard-viewer chain, an application must call the [ChangeClipboardChain](../vs140/CWnd--ChangeClipboardChain.md) member function.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::ChangeClipboardChain](../vs140/CWnd--ChangeClipboardChain.md)   
 [SetClipboardViewer](http://msdn.microsoft.com/library/windows/desktop/ms649052)