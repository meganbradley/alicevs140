---
title: "CWnd::GetScrollLimit"
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
ms.assetid: 8d0e3d93-5088-46c6-a0cd-f805021fcb30
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::GetScrollLimit
Call this member function to retrieve the maximum scrolling position of the scroll bar.  
  
## Syntax  
  
```  
  
      int GetScrollLimit(  
   int nBar   
);  
```  
  
#### Parameters  
 `nBar`  
 Specifies the type of scroll bar. The parameter can take one of the following values:  
  
-   **SB_HORZ** Retrieves the scroll limit of the horizontal scroll bar.  
  
-   **SB_VERT** Retrieves the scroll limit of the vertical scroll bar.  
  
## Return Value  
 Specifies the maximum position of a scroll bar if successful; otherwise 0.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CScrollBar::GetScrollLimit](../vs140/CScrollBar--GetScrollLimit.md)