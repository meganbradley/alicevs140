---
title: "CDocTemplate::InitialUpdateFrame"
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
ms.assetid: a84ad3ae-f919-4f60-9198-87cd38396289
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocTemplate::InitialUpdateFrame
Initializes the frame window, and optionally makes it visible.  
  
## Syntax  
  
```  
  
      virtual void InitialUpdateFrame(  
   CFrameWnd* pFrame,  
   CDocument* pDoc,  
   BOOL bMakeVisible = TRUE   
);  
```  
  
#### Parameters  
 `pFrame`  
 The frame window that needs the initial update.  
  
 `pDoc`  
 The document to which the frame is associated. Can be **NULL**.  
  
 `bMakeVisible`  
 Indicates whether the frame should become visible and active.  
  
## Remarks  
 Call **IntitialUpdateFrame** after creating a new frame with `CreateNewFrame`. Calling this function causes the views in that frame window to receive their `OnInitialUpdate` calls. Also, if there was not previously an active view, the primary view of the frame window is made active; the primary view is a view with a child ID of **AFX_IDW_PANE_FIRST**. Finally, the frame window is made visible if `bMakeVisible` is non-zero. If `bMakeVisible` is zero, the current focus and visible state of the frame window will remain unchanged.  
  
 It is not necessary to call this function when using the framework's implementation of File New and File Open.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocTemplate Class](../vs140/CDocTemplate-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CView::OnInitialUpdate](../vs140/CView--OnInitialUpdate.md)   
 [CFrameWnd::SetActiveView](../vs140/CFrameWnd--SetActiveView.md)   
 [CDocTemplate::CreateNewFrame](../vs140/CDocTemplate--CreateNewFrame.md)