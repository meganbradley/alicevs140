---
title: "COleIPFrameWnd::OnCreateControlBars"
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
ms.assetid: 477cfce5-3d93-4430-a93d-e027de28d54c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleIPFrameWnd::OnCreateControlBars
The framework calls the `OnCreateControlBars` function when an item is activated for in-place editing.  
  
## Syntax  
  
```  
  
      virtual BOOL OnCreateControlBars(  
   CWnd* pWndFrame,  
   CWnd* pWndDoc   
);  
virtual BOOL OnCreateControlBars(  
   CFrameWnd* pWndFrame,  
   CFrameWnd* pWndDoc   
);  
```  
  
#### Parameters  
 *pWndFrame*  
 Pointer to the container application's frame window.  
  
 *pWndDoc*  
 Pointer to the container's document-level window. Can be **NULL** if the container is an SDI application.  
  
## Return Value  
 Nonzero on success; otherwise, 0.  
  
## Remarks  
 The default implementation does nothing. Override this function to perform any special processing required when control bars are created.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleIPFrameWnd Class](../vs140/COleIPFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerDoc::ActivateInPlace](../vs140/COleServerDoc--ActivateInPlace.md)