---
title: "CWnd::EnableScrollBar"
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
ms.assetid: f591cb54-58b2-45cb-9420-cffc010066ef
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::EnableScrollBar
Enables or disables one or both arrows of a scroll bar.  
  
## Syntax  
  
```  
  
      BOOL EnableScrollBar(  
   int nSBFlags,  
   UINT nArrowFlags = ESB_ENABLE_BOTH   
);  
```  
  
#### Parameters  
 *nSBFlags*  
 Specifies the scroll-bar type. Can have one of the following values:  
  
-   **SB_BOTH** Enables or disables the arrows of the horizontal and vertical scroll bars associated with the window.  
  
-   **SB_HORZ** Enables or disables the arrows of the horizontal scroll bar associated with the window.  
  
-   **SB_VERT** Enables or disables the arrows of the vertical scroll bar associated with the window.  
  
 `nArrowFlags`  
 Specifies whether the scroll-bar arrows are enabled or disabled and which arrows are enabled or disabled. Can have one of the following values:  
  
-   **ESB_ENABLE_BOTH** Enables both arrows of a scroll bar (default).  
  
-   **ESB_DISABLE_LTUP** Disables the left arrow of a horizontal scroll bar or the up arrow of a vertical scroll bar.  
  
-   **ESB_DISABLE_RTDN** Disables the right arrow of a horizontal scroll bar or the down arrow of a vertical scroll bar.  
  
-   **ESB_DISABLE_BOTH** Disables both arrows of a scroll bar.  
  
## Return Value  
 Nonzero if the arrows are enabled or disabled as specified. Otherwise it is 0, which indicates that the arrows are already in the requested state or that an error occurred.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::ShowScrollBar](../vs140/CWnd--ShowScrollBar.md)   
 [CScrollBar::EnableScrollBar](../vs140/CScrollBar--EnableScrollBar.md)