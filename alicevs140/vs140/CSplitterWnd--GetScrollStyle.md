---
title: "CSplitterWnd::GetScrollStyle"
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
ms.assetid: 632de700-15fe-4b00-b771-11e446dbc0e0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSplitterWnd::GetScrollStyle
Returns the shared scroll-bar style for the splitter window.  
  
## Syntax  
  
```  
  
DWORD GetScrollStyle( ) const;  
```  
  
## Return Value  
 One or more of the following windows style flags, if successful:  
  
-   **WS_HSCROLL** If the splitter currently manages shared horizontal scroll bars.  
  
-   **WS_VSCROLL** If the splitter currently manages shared vertical scroll bars.  
  
 If zero, the splitter window does not currently manage any shared scroll bars.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CSplitterWnd Class](../vs140/CSplitterWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSplitterWnd::SetScrollStyle](../vs140/CSplitterWnd--SetScrollStyle.md)