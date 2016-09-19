---
title: "CFrameWnd::GetActiveView"
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
ms.assetid: 1b18d845-e722-4081-b05b-4679d67aa001
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWnd::GetActiveView
Call this member function to obtain a pointer to the active view (if any) attached to a frame window (`CFrameWnd`).  
  
## Syntax  
  
```  
  
CView* GetActiveView( ) const;  
```  
  
## Return Value  
 A pointer to the current [CView](../vs140/CView-Class.md). If there is no current view, returns **NULL**.  
  
## Remarks  
 This function returns **NULL** when called for an MDI main frame window (`CMDIFrameWnd`). In an MDI application, the MDI main frame window does not have a view associated with it. Instead, each individual child window (`CMDIChildWnd`) has one or more associated views. The active view in an MDI application can be obtained by first finding the active MDI child window and then finding the active view for that child window. The active MDI child window can be found by calling the function `MDIGetActive` or **GetActiveFrame** as demonstrated in the following:  
  
 [!CODE [NVC_MFCWindowing#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#2)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CFrameWnd Class](../vs140/CFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFrameWnd::SetActiveView](../vs140/CFrameWnd--SetActiveView.md)   
 [CFrameWnd::GetActiveDocument](../vs140/CFrameWnd--GetActiveDocument.md)