---
title: "COleDropTarget::OnDragOver"
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
ms.assetid: d50c6fed-01ee-46ed-8b4f-0e4c00aeb174
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDropTarget::OnDragOver
Called by the framework when the cursor is dragged over the window.  
  
## Syntax  
  
```  
  
      virtual DROPEFFECT OnDragOver(  
   CWnd* pWnd,  
   COleDataObject* pDataObject,  
   DWORD dwKeyState,  
   CPoint point   
);  
```  
  
#### Parameters  
 `pWnd`  
 Points to the window that the cursor is over.  
  
 `pDataObject`  
 Points to the data object that contains the data to be dropped.  
  
 `dwKeyState`  
 Contains the state of the modifier keys. This is a combination of any number of the following: **MK_CONTROL**, **MK_SHIFT**, **MK_ALT**, **MK_LBUTTON**, **MK_MBUTTON**, and **MK_RBUTTON**.  
  
 `point`  
 Contains the current location of the cursor in client coordinates.  
  
## Return Value  
 The effect that would result if a drop were attempted at the location specified by `point`. It can be one or more of the following:  
  
-   `DROPEFFECT_NONE` A drop would not be allowed.  
  
-   `DROPEFFECT_COPY` A copy operation would be performed.  
  
-   `DROPEFFECT_MOVE` A move operation would be performed.  
  
-   `DROPEFFECT_LINK` A link from the dropped data to the original data would be established.  
  
-   `DROPEFFECT_SCROLL` Indicates that a drag scroll operation is about to occur or is occurring in the target.  
  
## Remarks  
 This function should be overridden to allow drop operations to occur in the window. The default implementation of this function calls [CView::OnDragOver](../vs140/CView--OnDragOver.md), which returns `DROPEFFECT_NONE` by default. Because this function is called frequently during a drag-and-drop operation, it should be optimized as much as possible.  
  
 For more information, see [IDropTarget::DragOver](http://msdn.microsoft.com/library/windows/desktop/ms680129) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFCOleContainer#21](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCOleContainer#21)]  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDropTarget Class](../vs140/COleDropTarget-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDropTarget::OnDragEnter](../vs140/COleDropTarget--OnDragEnter.md)   
 [COleDropTarget::OnDragLeave](../vs140/COleDropTarget--OnDragLeave.md)   
 [COleDropTarget::OnDrop](../vs140/COleDropTarget--OnDrop.md)   
 [COleDropTarget::OnDropEx](../vs140/COleDropTarget--OnDropEx.md)