---
title: "CMDIChildWnd::MDIActivate"
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
ms.assetid: 763f1a7d-8c85-4774-9916-d803ba6f156d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIChildWnd::MDIActivate
Call this member function to activate an MDI child window independently of the MDI frame window.  
  
## Syntax  
  
```  
  
void MDIActivate( );  
```  
  
## Remarks  
 When the frame becomes active, the child window that was last activated will be activated as well.  
  
## Example  
 See the example for [CMDIFrameWnd::GetWindowMenuPopup](../vs140/CMDIFrameWnd--GetWindowMenuPopup.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMDIChildWnd Class](../vs140/CMDIChildWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMDIFrameWnd::MDIGetActive](../vs140/CMDIFrameWnd--MDIGetActive.md)   
 [CWnd::OnNcActivate](../vs140/CWnd--OnNcActivate.md)   
 [CMDIFrameWnd::MDINext](../vs140/CMDIFrameWnd--MDINext.md)   
 [WM_MDIACTIVATE](http://msdn.microsoft.com/library/windows/desktop/ms644911)