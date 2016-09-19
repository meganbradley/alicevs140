---
title: "CMDIChildWnd::MDIMaximize"
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
ms.assetid: 6aee4398-f959-473e-907f-96da6faac4dd
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIChildWnd::MDIMaximize
Call this member function to maximize an MDI child window.  
  
## Syntax  
  
```  
  
void MDIMaximize( );  
```  
  
## Remarks  
 When a child window is maximized, Windows resizes it to make its client area fill the client area of the frame window. Windows places the child window's Control menu in the frame's menu bar so that the user can restore or close the child window and adds the title of the child window to the frame-window title.  
  
## Example  
 [!CODE [NVC_MFCWindowing#11](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#11)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMDIChildWnd Class](../vs140/CMDIChildWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [WM_MDIMAXIMIZE](http://msdn.microsoft.com/library/windows/desktop/ms644917)   
 [CMDIChildWnd::MDIRestore](../vs140/CMDIChildWnd--MDIRestore.md)