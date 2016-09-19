---
title: "COleDropTarget::OnDragLeave"
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
ms.assetid: fe555e6a-0bdf-42fe-8412-fc187c6bc73c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDropTarget::OnDragLeave
Called by the framework when the cursor leaves the window while a dragging operation is in effect.  
  
## Syntax  
  
```  
  
      virtual void OnDragLeave(  
   CWnd* pWnd   
);  
```  
  
#### Parameters  
 `pWnd`  
 Points to the window the cursor is leaving.  
  
## Remarks  
 Override this function if you want special behavior when the drag operation leaves the specified window. The default implementation of this function calls [CView::OnDragLeave](../vs140/CView--OnDragLeave.md).  
  
 For more information, see [IDropTarget::DragLeave](http://msdn.microsoft.com/library/windows/desktop/ms680110) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDropTarget Class](../vs140/COleDropTarget-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDropTarget::OnDragEnter](../vs140/COleDropTarget--OnDragEnter.md)   
 [COleDropTarget::OnDragOver](../vs140/COleDropTarget--OnDragOver.md)   
 [COleDropTarget::OnDrop](../vs140/COleDropTarget--OnDrop.md)   
 [COleDropTarget::OnDropEx](../vs140/COleDropTarget--OnDropEx.md)