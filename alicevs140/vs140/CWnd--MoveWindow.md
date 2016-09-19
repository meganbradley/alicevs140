---
title: "CWnd::MoveWindow"
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
ms.assetid: 1b644e6d-ed92-421f-b8e6-ab95d35f8e51
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::MoveWindow
Changes the position and dimensions.  
  
## Syntax  
  
```  
  
      void MoveWindow(  
   int x,  
   int y,  
   int nWidth,  
   int nHeight,  
   BOOL bRepaint = TRUE   
);  
void MoveWindow(  
   LPCRECT lpRect,  
   BOOL bRepaint = TRUE   
);  
```  
  
#### Parameters  
 *x*  
 Specifies the new position of the left side of the `CWnd`.  
  
 *y*  
 Specifies the new position of the top of the `CWnd`.  
  
 `nWidth`  
 Specifies the new width of the `CWnd`.  
  
 `nHeight`  
 Specifies the new height of the `CWnd`.  
  
 `bRepaint`  
 Specifies whether `CWnd` is to be repainted. If **TRUE**, `CWnd` receives a [WM_PAINT](http://msdn.microsoft.com/library/windows/desktop/dd145213) message in its [OnPaint](../vs140/CWnd--OnPaint.md) message handler as usual. If this parameter is **FALSE**, no repainting of any kind occurs. This applies to the client area, to the nonclient area (including the title and scroll bars), and to any part of the parent window uncovered as a result of `CWnd`'s move. When this parameter is **FALSE**, the application must explicitly invalidate or redraw any parts of `CWnd` and parent window that must be redrawn.  
  
 `lpRect`  
 The [CRect](../vs140/CRect-Class.md) object or [RECT](../vs140/RECT-Structure.md) structure that specifies the new size and position.  
  
## Remarks  
 For a top-level `CWnd` object, the *x* and *y* parameters are relative to the upper-left corner of the screen. For a child `CWnd` object, they are relative to the upper-left corner of the parent window's client area.  
  
 The `MoveWindow` function sends the [WM_GETMINMAXINFO](../vs140/CWnd--OnGetMinMaxInfo.md) message. Handling this message gives `CWnd` the opportunity to modify the default values for the largest and smallest possible windows. If the parameters to the `MoveWindow` member function exceed these values, the values can be replaced by the minimum or maximum values in the `WM_GETMINMAXINFO` handler.  
  
## Example  
 See the example for [CWnd::ClientToScreen](../vs140/CWnd--ClientToScreen.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::SetWindowPos](../vs140/CWnd--SetWindowPos.md)   
 [CWnd::OnGetMinMaxInfo](../vs140/CWnd--OnGetMinMaxInfo.md)   
 [MoveWindow](http://msdn.microsoft.com/library/windows/desktop/ms633534)