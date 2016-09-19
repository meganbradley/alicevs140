---
title: "CFrameWnd::InitialUpdateFrame"
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
ms.assetid: e2a045cf-c6ec-4e9e-b64f-fde1d6f5fc49
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWnd::InitialUpdateFrame
Call **IntitialUpdateFrame** after creating a new frame with **Create**.  
  
## Syntax  
  
```  
  
      void InitialUpdateFrame(  
   CDocument* pDoc,  
   BOOL bMakeVisible   
);  
```  
  
#### Parameters  
 `pDoc`  
 Points to the document to which the frame window is associated. Can be **NULL**.  
  
 `bMakeVisible`  
 If **TRUE**, indicates that the frame should become visible and active. If **FALSE**, no descendants are made visible.  
  
## Remarks  
 This causes all views in that frame window to receive their `OnInitialUpdate` calls.  
  
 Also, if there was not previously an active view, the primary view of the frame window is made active. The primary view is a view with a child ID of **AFX_IDW_PANE_FIRST**. Finally, the frame window is made visible if `bMakeVisible` is nonzero. If `bMakeVisible` is 0, the current focus and visible state of the frame window will remain unchanged. It is not necessary to call this function when using the framework's implementation of File New and File Open.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CFrameWnd Class](../vs140/CFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CView::OnInitialUpdate](../vs140/CView--OnInitialUpdate.md)   
 [CFrameWnd::SetActiveView](../vs140/CFrameWnd--SetActiveView.md)   
 [CDocTemplate::CreateNewFrame](../vs140/CDocTemplate--CreateNewFrame.md)