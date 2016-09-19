---
title: "CView::OnDrop"
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
ms.assetid: dfd10d4a-fa25-4b8e-9f7d-8b7f93273f11
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CView::OnDrop
Called by the framework when the user releases a data object over a valid drop target.  
  
## Syntax  
  
```  
  
      virtual BOOL OnDrop(  
   COleDataObject* pDataObject,  
   DROPEFFECT dropEffect,  
   CPoint point   
);  
```  
  
#### Parameters  
 `pDataObject`  
 Points to the [COleDataObject](../vs140/COleDataObject-Class.md) that is dropped into the drop target.  
  
 `dropEffect`  
 The drop effect that the user has requested.  
  
-   `DROPEFFECT_COPY` Creates a copy of the data object being dropped.  
  
-   `DROPEFFECT_MOVE` Moves the data object to the current mouse location.  
  
-   `DROPEFFECT_LINK` Creates a link between a data object and its server.  
  
 `point`  
 The current mouse position relative to the view client area.  
  
## Return Value  
 Nonzero if the drop was successful; otherwise 0.  
  
## Remarks  
 The default implementation does nothing and returns **FALSE**.  
  
 Override this function to implement the effect of an OLE drop into the client area of the view. The data object can be examined via `pDataObject` for Clipboard data formats and data dropped at the specified point.  
  
> [!NOTE]
>  The framework does not call this function if there is an override to [OnDropEx](../vs140/CView--OnDropEx.md) in this view class.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CView Class](../vs140/CView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CView::OnDragEnter](../vs140/CView--OnDragEnter.md)   
 [CView::OnDragOver](../vs140/CView--OnDragOver.md)   
 [CView::OnDropEx](../vs140/CView--OnDropEx.md)   
 [CView::OnDragLeave](../vs140/CView--OnDragLeave.md)   
 [COleDropTarget::OnDrop](../vs140/COleDropTarget--OnDrop.md)