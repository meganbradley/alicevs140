---
title: "CWnd::SetActiveWindow"
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
ms.assetid: 0412ac71-cbb1-4f25-bade-56db1f92109a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::SetActiveWindow
Makes `CWnd` the active window.  
  
## Syntax  
  
```  
  
CWnd* SetActiveWindow( );  
```  
  
## Return Value  
 The window that was previously active.  
  
 The returned pointer may be temporary and should not be stored for later use.  
  
## Remarks  
 The `SetActiveWindow` member function should be used with care since it allows an application to arbitrarily take over the active window and input focus. Normally, Windows takes care of all activation.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [SetActiveWindow](http://msdn.microsoft.com/library/windows/desktop/ms646311)   
 [CWnd::GetActiveWindow](../vs140/CWnd--GetActiveWindow.md)