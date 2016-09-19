---
title: "CScrollView::ScrollToPosition"
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
ms.assetid: dfd050bd-b96d-4fc9-8e30-7a137f0ba12d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CScrollView::ScrollToPosition
Call `ScrollToPosition` to scroll to a given point in the view.  
  
## Syntax  
  
```  
  
      void ScrollToPosition(  
   POINT pt   
);  
```  
  
#### Parameters  
 `pt`  
 The point to scroll to, in logical units. The **x** member must be a positive value (greater than or equal to 0, up to the total size of the view). The same is true for the **y** member when the mapping mode is `MM_TEXT`. The **y** member is negative in mapping modes other than `MM_TEXT`.  
  
## Remarks  
 The view will be scrolled so that this point is at the upper-left corner of the window. This member function must not be called if the view is scaled to fit.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CScrollView Class](../vs140/CScrollView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CScrollView::GetDeviceScrollPosition](../vs140/CScrollView--GetDeviceScrollPosition.md)   
 [CScrollView::SetScaleToFitSize](../vs140/CScrollView--SetScaleToFitSize.md)   
 [CScrollView::SetScrollSizes](../vs140/CScrollView--SetScrollSizes.md)