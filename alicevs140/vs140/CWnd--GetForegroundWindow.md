---
title: "CWnd::GetForegroundWindow"
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
ms.assetid: 86b91e20-d7e9-4b8a-9dfc-743966c08caf
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::GetForegroundWindow
Returns a pointer to the foreground window (the window with which the user is currently working).  
  
## Syntax  
  
```  
  
static CWnd* PASCAL GetForegroundWindow( );  
```  
  
## Return Value  
 A pointer to the foreground window. This may be a temporary `CWnd` object.  
  
## Remarks  
 The foreground window applies only to top-level windows (frame windows or dialog boxes).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::SetForegroundWindow](../vs140/CWnd--SetForegroundWindow.md)