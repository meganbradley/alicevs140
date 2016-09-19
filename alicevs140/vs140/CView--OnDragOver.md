---
title: "CView::OnDragOver"
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
ms.assetid: 8ff44539-018a-4692-9dc3-48b8a2f1d140
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CView::OnDragOver
Called by the framework during a drag operation when the mouse is moved over the drop target window.  
  
## Syntax  
  
```  
  
      virtual DROPEFFECT OnDragOver(  
   COleDataObject* pDataObject,  
   DWORD dwKeyState,  
   CPoint point   
);  
```  
  
#### Parameters  
 `pDataObject`  
 Points to the [COleDataObject](../vs140/COleDataObject-Class.md) being dragged over the drop target.  
  
 `dwKeyState`  
 Contains the state of the modifier keys. This is a combination of any number of the following: **MK_CONTROL**, **MK_SHIFT**, **MK_ALT**, **MK_LBUTTON**, **MK_MBUTTON**, and **MK_RBUTTON**.  
  
 `point`  
 The current mouse position relative to the view client area.  
  
## Return Value  
 A value from the `DROPEFFECT` enumerated type, which indicates the type of drop that would occur if the user dropped the object at this position. The type of drop often depends on the current key state as indicated by `dwKeyState`. A standard mapping of keystates to `DROPEFFECT` values is:  
  
-   `DROPEFFECT_NONE` The data object cannot be dropped in this window.  
  
-   `DROPEFFECT_LINK` for **MK_CONTROL &#124; MK_SHIFT** Creates a linkage between the object and its server.  
  
-   `DROPEFFECT_COPY` for **MK_CONTROL** Creates a copy of the dropped object.  
  
-   `DROPEFFECT_MOVE` for **MK_ALT** Creates a copy of the dropped object and delete the original object. This is typically the default drop effect, when the view can accept the data object.  
  
 For more information, see the MFC Advanced Concepts sample [OCLIENT](../vs140/Visual-C---Samples.md).  
  
## Remarks  
 The default implementation is to do nothing and return `DROPEFFECT_NONE`.  
  
 Override this function to give the user visual feedback during the drag operation. Since this function is called continuously, any code contained within it should be optimized as much as possible. For more information, see the article [Drag and Drop: Implementing a Drop Target](../vs140/Drag-and-Drop--Implementing-a-Drop-Target.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CView Class](../vs140/CView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CView::OnDragEnter](../vs140/CView--OnDragEnter.md)   
 [CView::OnDrop](../vs140/CView--OnDrop.md)   
 [CView::OnDropEx](../vs140/CView--OnDropEx.md)   
 [CView::OnDragLeave](../vs140/CView--OnDragLeave.md)   
 [COleDropTarget::OnDragOver](../vs140/COleDropTarget--OnDragOver.md)