---
title: "CWnd::Invalidate"
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
ms.assetid: 104a3e69-ef04-480f-bead-55617f284afb
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::Invalidate
Invalidates the entire client area of `CWnd`.  
  
## Syntax  
  
```  
  
      void Invalidate(  
   BOOL bErase = TRUE   
);  
```  
  
#### Parameters  
 `bErase`  
 Specifies whether the background within the update region is to be erased.  
  
## Remarks  
 The client area is marked for painting when the next [WM_PAINT](../vs140/CWnd--OnPaint.md) message occurs. The region can also be validated before a `WM_PAINT` message occurs by the [ValidateRect](../vs140/CWnd--ValidateRect.md) or [ValidateRgn](../vs140/CWnd--ValidateRgn.md) member function.  
  
 The `bErase` parameter specifies whether the background within the update area is to be erased when the update region is processed. If `bErase` is **TRUE**, the background is erased when the [BeginPaint](../vs140/CWnd--BeginPaint.md) member function is called; if `bErase` is **FALSE**, the background remains unchanged. If `bErase` is **TRUE** for any part of the update region, the background in the entire region, not just in the given part, is erased.  
  
 Windows sends a [WM_PAINT](../vs140/CWnd--OnPaint.md) message whenever the `CWnd` update region is not empty and there are no other messages in the application queue for that window.  
  
## Example  
 See the example for [CWnd::UpdateWindow](../vs140/CWnd--UpdateWindow.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::BeginPaint](../vs140/CWnd--BeginPaint.md)   
 [CWnd::ValidateRect](../vs140/CWnd--ValidateRect.md)   
 [CWnd::ValidateRgn](../vs140/CWnd--ValidateRgn.md)   
 [InvalidateRect](http://msdn.microsoft.com/library/windows/desktop/dd145002)   
 [CWnd::InvalidateRect](../vs140/CWnd--InvalidateRect.md)   
 [CWnd::InvalidateRgn](../vs140/CWnd--InvalidateRgn.md)