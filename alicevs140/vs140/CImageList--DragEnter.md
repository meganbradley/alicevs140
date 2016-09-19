---
title: "CImageList::DragEnter"
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
ms.assetid: 04113020-fc81-4683-b0e8-1500962ab84b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImageList::DragEnter
During a drag operation, locks updates to the window specified by `pWndLock` and displays the drag image at the position specified by `point`.  
  
## Syntax  
  
```  
  
      static BOOL PASCAL DragEnter(  
   CWnd* pWndLock,  
   CPoint point   
);  
```  
  
#### Parameters  
 `pWndLock`  
 Pointer to the window that owns the drag image.  
  
 `point`  
 Position at which to display the drag image. Coordinates are relative to the upper left corner of the window (not the client area).  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 The coordinates are relative to the window's upper left corner, so you must compensate for the widths of window elements, such as the border, title bar, and menu bar, when specifying the coordinates.  
  
 If `pWndLock` is **NULL**, this function draws the image in the display context associated with the desktop window, and coordinates are relative to the upper left corner of the screen.  
  
 This function locks all other updates to the given window during the drag operation. If you need to do any drawing during a drag operation, such as highlighting the target of a drag-and-drop operation, you can temporarily hide the dragged image by using the [CImageList::DragLeave](../vs140/CImageList--DragLeave.md) function.  
  
## Example  
 See the example for [CImageList::BeginDrag](../vs140/CImageList--BeginDrag.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CImageList Class](../vs140/CImageList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CImageList::BeginDrag](../vs140/CImageList--BeginDrag.md)   
 [CImageList::EndDrag](../vs140/CImageList--EndDrag.md)   
 [CImageList::DragMove](../vs140/CImageList--DragMove.md)   
 [CImageList::DragLeave](../vs140/CImageList--DragLeave.md)