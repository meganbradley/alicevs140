---
title: "CFrameWnd::GetActiveFrame"
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
ms.assetid: 1fc338eb-76d0-4fb6-883e-cbeecb9b0539
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWnd::GetActiveFrame
Call this member function to obtain a pointer to the active multiple document interface (MDI) child window of an MDI frame window.  
  
## Syntax  
  
```  
  
virtual CFrameWnd* GetActiveFrame( );  
```  
  
## Return Value  
 A pointer to the active MDI child window. If the application is an SDI application, or the MDI frame window has no active document, the implicit **this** pointer will be returned.  
  
## Remarks  
 If there is no active MDI child or the application is a single document interface (SDI), the implicit **this** pointer is returned.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CFrameWnd Class](../vs140/CFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFrameWnd::GetActiveView](../vs140/CFrameWnd--GetActiveView.md)   
 [CFrameWnd::GetActiveDocument](../vs140/CFrameWnd--GetActiveDocument.md)   
 [CMDIFrameWnd Class](../vs140/CMDIFrameWnd-Class.md)