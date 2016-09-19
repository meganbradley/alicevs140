---
title: "CView::OnDragScroll"
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
ms.assetid: 526fc8cb-57c5-4a5d-93d9-93b1e8d46c69
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CView::OnDragScroll
Called by the framework before calling [OnDragEnter](../vs140/CView--OnDragEnter.md) or [OnDragOver](../vs140/CView--OnDragOver.md) to determine whether the point is in the scrolling region.  
  
## Syntax  
  
```  
  
      virtual DROPEFFECT OnDragScroll(  
   DWORD dwKeyState,  
   CPoint point   
);  
```  
  
#### Parameters  
 `dwKeyState`  
 Contains the state of the modifier keys. This is a combination of any number of the following: **MK_CONTROL**, **MK_SHIFT**, **MK_ALT**, **MK_LBUTTON**, **MK_MBUTTON**, and **MK_RBUTTON**.  
  
 `point`  
 Contains the location of the cursor, in pixels, relative to the screen.  
  
## Return Value  
 A value from the `DROPEFFECT` enumerated type, which indicates the type of drop that would occur if the user dropped the object at this position. The type of drop usually depends on the current key state indicated by `dwKeyState`. A standard mapping of keystates to `DROPEFFECT` values is:  
  
-   `DROPEFFECT_NONE` The data object cannot be dropped in this window.  
  
-   `DROPEFFECT_LINK` for **MK_CONTROL &#124; MK_SHIFT** Creates a linkage between the object and its server.  
  
-   `DROPEFFECT_COPY` for **MK_CONTROL** Creates a copy of the dropped object.  
  
-   `DROPEFFECT_MOVE` for **MK_ALT** Creates a copy of the dropped object and delete the original object.  
  
-   `DROPEFFECT_SCROLL` Indicates that a drag scroll operation is about to occur or is occurring in the target view.  
  
 For more information, see the MFC Advanced Concepts sample [OCLIENT](../vs140/Visual-C---Samples.md).  
  
## Remarks  
 Override this function when you want to provide special behavior for this event. The default implementation automatically scrolls windows when the cursor is dragged into the default scroll region inside the border of each window.For more information, see the article [Drag and Drop: Implementing a Drop Target](../vs140/Drag-and-Drop--Implementing-a-Drop-Target.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CView Class](../vs140/CView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CView::OnDragEnter](../vs140/CView--OnDragEnter.md)   
 [CView::OnDragOver](../vs140/CView--OnDragOver.md)   
 [CView::OnDrop](../vs140/CView--OnDrop.md)   
 [CView::OnDragLeave](../vs140/CView--OnDragLeave.md)   
 [COleDropTarget::OnDragScroll](../vs140/COleDropTarget--OnDragScroll.md)