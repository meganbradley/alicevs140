---
title: "CWnd::SetScrollInfo"
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
ms.assetid: f994a9e8-5429-4808-be60-563fe6616fe8
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::SetScrollInfo
Call this member function to set the information that the `SCROLLINFO` structure maintains about a scroll bar.  
  
## Syntax  
  
```  
  
      BOOL SetScrollInfo(  
   int nBar,  
   LPSCROLLINFO lpScrollInfo,  
   BOOL bRedraw = TRUE   
);  
```  
  
#### Parameters  
 `nBar`  
 Specifies whether the scroll bar is a control or part of a window's nonclient area. If it is part of the nonclient area, nBar also indicates whether the scroll bar is positioned horizontally, vertically, or both. It must be one of the following:  
  
-   **SB_CTL** Contains the parameters for a scroll bar control. The `m_hWnd` data member must be the handle of the scroll bar control.  
  
-   **SB_HORZ** Specifies that the window is a horizontal scroll bar.  
  
-   **SB_VERT** Specifies that the window is a vertical scroll bar.  
  
 `lpScrollInfo`  
 A pointer to a [SCROLLINFO](http://msdn.microsoft.com/library/windows/desktop/bb787537) structure. See the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for more information about this structure.  
  
 `bRedraw`  
 Specifies whether the scroll bar should be redrawn to reflect the new position. If `bRedraw` is **TRUE**, the scroll bar is redrawn. If it is **FALSE**, it is not redrawn. The scroll bar is redrawn by default.  
  
## Return Value  
 If successful, the return is **TRUE**. Otherwise, it is **FALSE**.  
  
## Remarks  
 The [SCROLLINFO](http://msdn.microsoft.com/library/windows/desktop/bb787537) structure contains information about a scroll bar, including the minimum and maximum scrolling positions, the page size, and the position of the scroll box (the thumb). See the `SCROLLINFO` structure topic in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for more information about changing the structure defaults.  
  
 The MFC Windows message handlers that indicate scroll-bar position, [CWnd::OnHScroll](../vs140/CWnd--OnHScroll.md) and [CWnd::OnVScroll](../vs140/CWnd--OnVScroll.md), provide only 16 bits of position data. [GetScrollInfo](../vs140/CWnd--GetScrollInfo.md) and `SetScrollInfo` provide 32 bits of scroll-bar position data. Thus, an application can call `GetScrollInfo` while processing either `CWnd::OnHScroll` or `CWnd::OnVScroll` to obtain 32-bit scroll-bar position data.  
  
> [!NOTE]
>  [CWnd::GetScrollInfo](../vs140/CWnd--GetScrollInfo.md) enables applications to use 32-bit scroll-bar positions.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::GetScrollInfo](../vs140/CWnd--GetScrollInfo.md)   
 [CWnd::SetScrollPos](../vs140/CWnd--SetScrollPos.md)   
 [CWnd::OnVScroll](../vs140/CWnd--OnVScroll.md)   
 [CWnd::OnHScroll](../vs140/CWnd--OnHScroll.md)   
 [SCROLLINFO](http://msdn.microsoft.com/library/windows/desktop/bb787537)