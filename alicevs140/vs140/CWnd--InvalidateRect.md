---
title: "CWnd::InvalidateRect"
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
ms.assetid: d7b0dec5-b92d-40f9-acc2-2455d747ea18
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::InvalidateRect
Invalidates the client area within the given rectangle by adding that rectangle to the `CWnd` update region.  
  
## Syntax  
  
```  
  
      void InvalidateRect(  
   LPCRECT lpRect,  
   BOOL bErase = TRUE   
);  
```  
  
#### Parameters  
 `lpRect`  
 Points to a `CRect` object or a [RECT](../vs140/RECT-Structure.md) structure that contains the rectangle (in client coordinates) to be added to the update region. If `lpRect` is **NULL**, the entire client area is added to the region.  
  
 `bErase`  
 Specifies whether the background within the update region is to be erased.  
  
## Remarks  
 The invalidated rectangle, along with all other areas in the update region, is marked for painting when the next [WM_PAINT](../vs140/CWnd--OnPaint.md) message is sent. The invalidated areas accumulate in the update region until the region is processed when the next `WM_PAINT` call occurs, or until the region is validated by the [ValidateRect](../vs140/CWnd--ValidateRect.md) or [ValidateRgn](../vs140/CWnd--ValidateRgn.md) member function.  
  
 The `bErase` parameter specifies whether the background within the update area is to be erased when the update region is processed. If `bErase` is **TRUE**, the background is erased when the [BeginPaint](../vs140/CWnd--BeginPaint.md) member function is called; if `bErase` is **FALSE**, the background remains unchanged. If `bErase` is **TRUE** for any part of the update region, the background in the entire region is erased, not just in the given part.  
  
 Windows sends a [WM_PAINT](../vs140/CWnd--OnPaint.md) message whenever the `CWnd` update region is not empty and there are no other messages in the application queue for that window.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::BeginPaint](../vs140/CWnd--BeginPaint.md)   
 [CWnd::ValidateRect](../vs140/CWnd--ValidateRect.md)   
 [CWnd::ValidateRgn](../vs140/CWnd--ValidateRgn.md)   
 [InvalidateRect](http://msdn.microsoft.com/library/windows/desktop/dd145002)   
 [CWnd::Invalidate](../vs140/CWnd--Invalidate.md)   
 [CWnd::InvalidateRgn](../vs140/CWnd--InvalidateRgn.md)