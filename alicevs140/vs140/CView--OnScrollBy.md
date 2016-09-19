---
title: "CView::OnScrollBy"
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
ms.assetid: 20dc769d-de57-4dea-834f-dfc3d0eb69d0
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CView::OnScrollBy
Called by the framework when the user views an area beyond the present view of the document, either by dragging an OLE item against the view's current borders or by manipulating the vertical or horizontal scrollbars.  
  
## Syntax  
  
```  
  
      virtual BOOL OnScrollBy(  
   CSize sizeScroll,  
   BOOL bDoScroll = TRUE   
);  
```  
  
#### Parameters  
 `sizeScroll`  
 Number of pixels scrolled horizontally and vertically.  
  
 `bDoScroll`  
 Determines whether scrolling of the view occurs. If **TRUE,** then scrolling takes place; if **FALSE**, then scrolling does not occur.  
  
## Return Value  
 Nonzero if the view was able to be scrolled; otherwise 0.  
  
## Remarks  
 In derived classes this method checks to see whether the view is scrollable in the direction the user requested and then updates the new region if necessary. This function is automatically called by [CWnd::OnHScroll](../vs140/CWnd--OnHScroll.md) and [CWnd::OnVScroll](../vs140/CWnd--OnVScroll.md) to perform the actual scrolling request.  
  
 The default implementation of this method does not change the view, but if it is not called, the view will not scroll in a `CScrollView`-derived class.  
  
 If the document width or height exceeds 32767 pixels, scrolling past 32767 will fail because `OnScrollBy` is called with an invalid `sizeScroll` argument.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CView Class](../vs140/CView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)