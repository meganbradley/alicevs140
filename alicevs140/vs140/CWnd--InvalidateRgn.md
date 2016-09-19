---
title: "CWnd::InvalidateRgn"
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
ms.assetid: e71c7d35-d96c-4b66-bb45-8cdc68abba9d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::InvalidateRgn
Invalidates the client area within the given region by adding it to the current update region of `CWnd`.  
  
## Syntax  
  
```  
  
      void InvalidateRgn(  
   CRgn* pRgn,  
   BOOL bErase = TRUE   
);  
```  
  
#### Parameters  
 `pRgn`  
 A pointer to a [CRgn](../vs140/CRgn-Class.md) object that identifies the region to be added to the update region. The region is assumed to have client coordinates. If this parameter is **NULL**, the entire client area is added to the update region.  
  
 `bErase`  
 Specifies whether the background within the update region is to be erased.  
  
## Remarks  
 The invalidated region, along with all other areas in the update region, is marked for painting when the [WM_PAINT](../vs140/CWnd--OnPaint.md) message is next sent. The invalidated areas accumulate in the update region until the region is processed when a `WM_PAINT` message is next sent, or until the region is validated by the [ValidateRect](../vs140/CWnd--ValidateRect.md) or [ValidateRgn](../vs140/CWnd--ValidateRgn.md) member function.  
  
 The `bErase` parameter specifies whether the background within the update area is to be erased when the update region is processed. If `bErase` is **TRUE**, the background is erased when the [BeginPaint](../vs140/CWnd--BeginPaint.md) member function is called; if `bErase` is **FALSE**, the background remains unchanged. If `bErase` is **TRUE** for any part of the update region, the background in the entire region, not just in the given part, is erased.  
  
 Windows sends a [WM_PAINT](../vs140/CWnd--OnPaint.md) message whenever the `CWnd` update region is not empty and there are no other messages in the application queue for that window.  
  
 The given region must have been previously created by one of the region functions.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::BeginPaint](../vs140/CWnd--BeginPaint.md)   
 [CWnd::ValidateRect](../vs140/CWnd--ValidateRect.md)   
 [CWnd::ValidateRgn](../vs140/CWnd--ValidateRgn.md)   
 [InvalidateRgn](http://msdn.microsoft.com/library/windows/desktop/dd145003)   
 [CWnd::Invalidate](../vs140/CWnd--Invalidate.md)   
 [CWnd::InvalidateRect](../vs140/CWnd--InvalidateRect.md)