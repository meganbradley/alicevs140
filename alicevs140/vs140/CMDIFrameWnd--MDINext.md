---
title: "CMDIFrameWnd::MDINext"
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
ms.assetid: 2c6c18a3-3041-4915-9def-322163d6cb09
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWnd::MDINext
Activates the child window immediately behind the currently active child window and places the currently active child window behind all other child windows.  
  
## Syntax  
  
```  
  
void MDINext( );  
```  
  
## Remarks  
 If the currently active MDI child window is maximized, the member function restores the currently active child and maximizes the newly activated child.  
  
## Example  
 [!CODE [NVC_MFCWindowing#18](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#18)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMDIFrameWnd Class](../vs140/CMDIFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMDIFrameWnd::MDIPrev](../vs140/CMDIFrameWnd--MDIPrev.md)   
 [CMDIFrameWnd::MDIActivate](../vs140/CMDIFrameWnd--MDIActivate.md)   
 [CMDIFrameWnd::MDIGetActive](../vs140/CMDIFrameWnd--MDIGetActive.md)   
 [WM_MDINEXT](http://msdn.microsoft.com/library/windows/desktop/ms644918)