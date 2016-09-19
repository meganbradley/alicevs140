---
title: "CWnd::GetFocus"
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
ms.assetid: de5fe96e-deb6-41e8-8be6-bdc08ceb252f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::GetFocus
Retrieves a pointer to the `CWnd` that currently has the input focus.  
  
## Syntax  
  
```  
  
static CWnd* PASCAL GetFocus( );  
```  
  
## Return Value  
 A pointer to the window that has the current focus, or **NULL** if there is no focus window.  
  
 The pointer may be temporary and should not be stored for later use.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::GetActiveWindow](../vs140/CWnd--GetActiveWindow.md)   
 [CWnd::GetCapture](../vs140/CWnd--GetCapture.md)   
 [CWnd::SetFocus](../vs140/CWnd--SetFocus.md)   
 [GetFocus](http://msdn.microsoft.com/library/windows/desktop/ms646294)