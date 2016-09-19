---
title: "CDockablePane::HitTest"
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
ms.assetid: a917d587-1b35-4b25-8c4e-787394894249
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockablePane::HitTest
Specifies the location in a pane where the user clicks a mouse.  
  
## Syntax  
  
```  
virtual int HitTest(  
    CPoint point,  
    BOOL bDetectCaption = FALSE  
);  
```  
  
#### Parameters  
 [in] `point`  
 Specifies the point to test.  
  
 [in] `bDetectCaption`  
 `TRUE` if `HTCAPTION` should be returned if the point is on the pane's caption; otherwise, `FALSE`.  
  
## Return Value  
 One of the following values:  
  
-   `HTNOWHERE` if `point` is not in the dockable pane.  
  
-   `HTCLIENT` if `point` is in the client area of the dockable pane.  
  
-   `HTCAPTION` if `point` is in the caption area of the dockable pane.  
  
-   `AFX_HTCLOSE` if `point` is on the close button.  
  
-   `HTMAXBUTTON` if `point` is on the pin button.  
  
## Requirements  
 **Header:** afxDockablePane.h  
  
## See Also  
 [CDockablePane Class](../vs140/CDockablePane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)