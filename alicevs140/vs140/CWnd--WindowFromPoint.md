---
title: "CWnd::WindowFromPoint"
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
ms.assetid: d2f7eae9-3895-40d0-9857-146fb24b1f08
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::WindowFromPoint
Retrieves the window that contains the specified point; `point` must specify the screen coordinates of a point on the screen.  
  
## Syntax  
  
```  
  
      static CWnd* PASCAL WindowFromPoint(  
   POINT point   
);  
```  
  
#### Parameters  
 `point`  
 Specifies a [CPoint](../vs140/CPoint-Class.md) object or [POINT](../vs140/POINT-Structure.md) data structure that defines the point to be checked.  
  
## Return Value  
 A pointer to the window object in which the point lies. It is **NULL** if no window exists at the given point. The returned pointer may be temporary and should not be stored for later use.  
  
## Remarks  
 `WindowFromPoint` does not retrieve a hidden or disabled window, even if the point is within the window. An application should use the [ChildWindowFromPoint](../vs140/CWnd--ChildWindowFromPoint.md) member function for a nonrestrictive search.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [WindowFromPoint](http://msdn.microsoft.com/library/windows/desktop/ms633558)   
 [CWnd::ChildWindowFromPoint](../vs140/CWnd--ChildWindowFromPoint.md)