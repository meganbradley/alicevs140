---
title: "CWnd::OnVScroll"
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
ms.assetid: 23cf0af9-41c8-4987-996e-199db0c2b3d6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnVScroll
The framework calls this member function when the user clicks the window's vertical scroll bar.  
  
## Syntax  
  
```  
  
      afx_msg void OnVScroll(  
   UINT nSBCode,  
   UINT nPos,  
   CScrollBar* pScrollBar   
);  
```  
  
#### Parameters  
 `nSBCode`  
 Specifies a scroll-bar code that indicates the user's scrolling request. This parameter can be one of the following:  
  
-   **SB_BOTTOM** Scroll to bottom.  
  
-   **SB_ENDSCROLL** End scroll.  
  
-   **SB_LINEDOWN** Scroll one line down.  
  
-   **SB_LINEUP** Scroll one line up.  
  
-   **SB_PAGEDOWN** Scroll one page down.  
  
-   **SB_PAGEUP** Scroll one page up.  
  
-   **SB_THUMBPOSITION** Scroll to the absolute position. The current position is provided in `nPos`.  
  
-   **SB_THUMBTRACK** Drag scroll box to specified position. The current position is provided in `nPos`.  
  
-   **SB_TOP** Scroll to top.  
  
 `nPos`  
 Contains the current scroll-box position if the scroll-bar code is **SB_THUMBPOSITION** or **SB_THUMBTRACK**; otherwise not used. Depending on the initial scroll range, `nPos` may be negative and should be cast to an `int` if necessary.  
  
 `pScrollBar`  
 If the scroll message came from a scroll-bar control, contains a pointer to the control. If the user clicked a window's scroll bar, this parameter is **NULL**. The pointer may be temporary and should not be stored for later use.  
  
## Remarks  
 `OnVScroll` typically is used by applications that give some feedback while the scroll box is being dragged.  
  
 If `OnVScroll` scrolls the contents of the `CWnd` object, it must also reset the position of the scroll box with the [SetScrollPos](../vs140/CWnd--SetScrollPos.md) member function.  
  
> [!NOTE]
>  This member function is called by the framework to allow your application to handle a Windows message. The parameters passed to your function reflect the parameters received by the framework when the message was received. If you call the base-class implementation of this function, that implementation will use the parameters originally passed with the message and not the parameters you supply to the function.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::SetScrollPos](../vs140/CWnd--SetScrollPos.md)   
 [CWnd::OnHScroll](../vs140/CWnd--OnHScroll.md)   
 [WM_VSCROLL](http://msdn.microsoft.com/library/windows/desktop/bb787577)