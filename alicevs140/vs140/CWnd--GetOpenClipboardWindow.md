---
title: "CWnd::GetOpenClipboardWindow"
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
ms.assetid: ff74977b-dabc-4bd2-bb47-18fbf4ef170d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::GetOpenClipboardWindow
Retrieves the handle of the window that currently has the Clipboard open.  
  
## Syntax  
  
```  
  
static CWnd* PASCAL GetOpenClipboardWindow( );  
```  
  
## Return Value  
 The handle of the window that currently has the Clipboard open if the function is successful; otherwise **NULL**.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::GetClipboardOwner](../vs140/CWnd--GetClipboardOwner.md)   
 [CWnd::GetClipboardViewer](../vs140/CWnd--GetClipboardViewer.md)   
 [CWnd::OpenClipboard](../vs140/CWnd--OpenClipboard.md)   
 [GetOpenClipboardWindow](http://msdn.microsoft.com/library/windows/desktop/ms649044)