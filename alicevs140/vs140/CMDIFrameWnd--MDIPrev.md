---
title: "CMDIFrameWnd::MDIPrev"
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
ms.assetid: bda20b09-bc25-495e-89c2-79968213abd0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWnd::MDIPrev
Activates the previous child window and places the currently active child window immediately behind it.  
  
## Syntax  
  
```  
  
void MDIPrev( );  
  
```  
  
## Remarks  
 If the currently active MDI child window is maximized, the member function restores the currently active child and maximizes the newly activated child.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMDIFrameWnd Class](../vs140/CMDIFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMDIFrameWnd::MDINext](../vs140/CMDIFrameWnd--MDINext.md)   
 [CMDIFrameWnd::MDIActivate](../vs140/CMDIFrameWnd--MDIActivate.md)   
 [CMDIFrameWnd::MDIGetActive](../vs140/CMDIFrameWnd--MDIGetActive.md)   
 [WM_MDINEXT](http://msdn.microsoft.com/library/windows/desktop/ms644918)