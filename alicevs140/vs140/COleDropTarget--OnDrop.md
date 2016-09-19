---
title: "COleDropTarget::OnDrop"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 3617813e-9cab-477b-8bca-eb25a0722bc9
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDropTarget::OnDrop
Called by the framework when a drop operation is to occur.  
  
## Syntax  
  
```  
  
      virtual BOOL OnDrop(  
   CWnd* pWnd,  
   COleDataObject* pDataObject,  
   DROPEFFECT dropEffect,  
   CPoint point   
);  
```  
  
#### Parameters  
 `pWnd`  
 Points to the window the cursor is currently over.  
  
 `pDataObject`  
 Points to the data object that contains the data to be dropped.  
  
 `dropEffect`  
 The effect that the user chose for the drop operation. It can be one or more of the following:  
  
-   `DROPEFFECT_COPY` A copy operation would be performed.  
  
-   `DROPEFFECT_MOVE` A move operation would be performed.  
  
-   `DROPEFFECT_LINK` A link from the dropped data to the original data would be established.  
  
 `point`  
 Contains the location of the cursor, in pixels, relative to the screen.  
  
## Return Value  
 Nonzero if the drop is successful; otherwise 0.  
  
## Remarks  
 The framework first calls [OnDropEx](../vs140/COleDropTarget--OnDropEx.md). If the `OnDropEx` function does not handle the drop, the framework then calls this member function, `OnDrop`. Typically, the application overrides [OnDropEx](../vs140/CView--OnDropEx.md) in the view class to handle right mouse-button drag and drop. Typically, the view class [OnDrop](../vs140/CView--OnDrop.md) is used to handle simple drag and drop.  
  
 The default implementation of `COleDropTarget::OnDrop` calls [CView::OnDrop](../vs140/CView--OnDrop.md), which simply returns **FALSE** by default.  
  
 For more information, see [IDropTarget::Drop](http://msdn.microsoft.com/library/windows/desktop/ms687242) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDropTarget Class](../vs140/COleDropTarget-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDropTarget::OnDragOver](../vs140/COleDropTarget--OnDragOver.md)   
 [COleDropTarget::OnDragEnter](../vs140/COleDropTarget--OnDragEnter.md)   
 [COleDropTarget::OnDropEx](../vs140/COleDropTarget--OnDropEx.md)