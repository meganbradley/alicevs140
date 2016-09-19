---
title: "CScrollBar::EnableScrollBar"
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
ms.assetid: 58db93fd-5df4-4bf0-bb01-7215274ca404
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CScrollBar::EnableScrollBar
Enables or disables one or both arrows of a scroll bar.  
  
## Syntax  
  
```  
  
      BOOL EnableScrollBar(  
   UINT nArrowFlags = ESB_ENABLE_BOTH   
);  
```  
  
#### Parameters  
 `nArrowFlags`  
 Specifies whether the scroll arrows are enabled or disabled and which arrows are enabled or disabled. This parameter can be one of the following values:  
  
-   **ESB_ENABLE_BOTH** Enables both arrows of a scroll bar.  
  
-   **ESB_DISABLE_LTUP** Disables the left arrow of a horizontal scroll bar or the up arrow of a vertical scroll bar.  
  
-   **ESB_DISABLE_RTDN** Disables the right arrow of a horizontal scroll bar or the down arrow of a vertical scroll bar.  
  
-   **ESB_DISABLE_BOTH** Disables both arrows of a scroll bar.  
  
## Return Value  
 Nonzero if the arrows are enabled or disabled as specified; otherwise 0, which indicates that the arrows are already in the requested state or that an error occurred.  
  
## Example  
 See the example for [CScrollBar::SetScrollRange](../vs140/CScrollBar--SetScrollRange.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CScrollBar Class](../vs140/CScrollBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::EnableScrollBar](../vs140/CWnd--EnableScrollBar.md)   
 [EnableScrollBar](http://msdn.microsoft.com/library/windows/desktop/bb787579)