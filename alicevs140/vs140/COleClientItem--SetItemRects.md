---
title: "COleClientItem::SetItemRects"
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
ms.assetid: 0e07932f-b126-4e1a-80e4-864f2b96d44c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::SetItemRects
Call this function to set the bounding rectangle or the visible rectangle of the OLE item.  
  
## Syntax  
  
```  
  
      BOOL SetItemRects(   
   LPCRECT lpPosRect = NULL,   
   LPCRECT lpClipRect = NULL    
);  
```  
  
#### Parameters  
 *lprcPosRect*  
 Pointer to the rectangle containing the bounds of the OLE item relative to its parent window, in client coordinates.  
  
 *lprcClipRect*  
 Pointer to the rectangle containing the bounds of the visible portion of the OLE item relative to its parent window, in client coordinates.  
  
## Return Value  
 Nonzero if successful; otherwise, 0.  
  
## Remarks  
 This function is called by the default implementation of the [OnChangeItemPosition](../vs140/COleClientItem--OnChangeItemPosition.md) member function. You should call this function whenever the position or visible portion of the OLE item changes. Usually this means that you call it from your view's [OnSize](../vs140/CWnd--OnSize.md) and [OnScrollBy](../vs140/CView--OnScrollBy.md) member functions.  
  
 For more information, see [IOleInPlaceObject::SetObjectRects](http://msdn.microsoft.com/library/windows/desktop/ms683767) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::OnChangeItemPosition](../vs140/COleClientItem--OnChangeItemPosition.md)   
 [COleClientItem::OnGetItemPosition](../vs140/COleClientItem--OnGetItemPosition.md)