---
title: "CView::OnDragEnter"
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
ms.assetid: fbee6a3a-fbfb-464a-a237-e9bd3c639585
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CView::OnDragEnter
Called by the framework when the mouse first enters the non-scrolling region of the drop target window.  
  
## Syntax  
  
```  
  
      virtual DROPEFFECT OnDragEnter(  
   COleDataObject* pDataObject,  
   DWORD dwKeyState,  
   CPoint point   
);  
```  
  
#### Parameters  
 `pDataObject`  
 Points to the [COleDataObject](../vs140/COleDataObject-Class.md) being dragged into the drop area of the view.  
  
 `dwKeyState`  
 Contains the state of the modifier keys. This is a combination of any number of the following: **MK_CONTROL**, **MK_SHIFT**, **MK_ALT**, **MK_LBUTTON**, **MK_MBUTTON**, and **MK_RBUTTON**.  
  
 `point`  
 The current mouse position relative to the client area of the view.  
  
## Return Value  
 A value from the `DROPEFFECT` enumerated type, which indicates the type of drop that would occur if the user dropped the object at this position. The type of drop usually depends on the current key state indicated by `dwKeyState`. A standard mapping of keystates to `DROPEFFECT` values is:  
  
-   `DROPEFFECT_NONE` The data object cannot be dropped in this window.  
  
-   `DROPEFFECT_LINK` for **MK_CONTROL &#124; MK_SHIFT** Creates a linkage between the object and its server.  
  
-   `DROPEFFECT_COPY` for **MK_CONTROL** Creates a copy of the dropped object.  
  
-   `DROPEFFECT_MOVE` for **MK_ALT** Creates a copy of the dropped object and delete the original object. This is typically the default drop effect, when the view can accept this data object.  
  
 For more information, see the MFC Advanced Concepts sample [OCLIENT](../vs140/Visual-C---Samples.md).  
  
## Remarks  
 Default implementation is to do nothing and return `DROPEFFECT_NONE`.  
  
 Override this function to prepare for future calls to the [OnDragOver](../vs140/CView--OnDragOver.md) member function. Any data required from the data object should be retrieved at this time for later use in the `OnDragOver` member function. The view should also be updated at this time to give the user visual feedback. For more information, see the article [Drag and Drop: Implementing a Drop Target](../vs140/Drag-and-Drop--Implementing-a-Drop-Target.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CView Class](../vs140/CView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CView::OnDragOver](../vs140/CView--OnDragOver.md)   
 [CView::OnDrop](../vs140/CView--OnDrop.md)   
 [CView::OnDropEx](../vs140/CView--OnDropEx.md)   
 [CView::OnDragLeave](../vs140/CView--OnDragLeave.md)   
 [COleDropTarget::OnDragEnter](../vs140/COleDropTarget--OnDragEnter.md)