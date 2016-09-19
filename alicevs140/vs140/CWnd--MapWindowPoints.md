---
title: "CWnd::MapWindowPoints"
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
ms.assetid: 567c017e-1137-4773-aa67-5f82574ba72d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::MapWindowPoints
Converts (maps) a set of points from the coordinate space of the `CWnd` to the coordinate space of another window.  
  
## Syntax  
  
```  
  
      void MapWindowPoints(  
   CWnd* pwndTo,  
   LPRECT lpRect   
) const;  
void MapWindowPoints(  
   CWnd* pwndTo,  
   LPPOINT lpPoint,  
   UINT nCount   
) const;  
```  
  
#### Parameters  
 *pwndTo*  
 Identifies the window to which points are converted. If this parameter is **NULL**, the points are converted to screen coordinates.  
  
 `lpRect`  
 Specifies the rectangle whose points are to be converted. The first version of this function is available only for Windows 3.1 and later.  
  
 `lpPoint`  
 A pointer to an array of [POINT](../vs140/POINT-Structure.md) structures that contain the set of points to be converted.  
  
 `nCount`  
 Specifies the number of **POINT** structures in the array pointed to by `lpPoint`.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::ClientToScreen](../vs140/CWnd--ClientToScreen.md)   
 [CWnd::ScreenToClient](../vs140/CWnd--ScreenToClient.md)   
 [MapWindowPoints](http://msdn.microsoft.com/library/windows/desktop/dd145046)