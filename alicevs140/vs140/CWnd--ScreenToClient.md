---
title: "CWnd::ScreenToClient"
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
ms.assetid: 6461c98a-7a9d-4d6c-905f-23fc13251651
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::ScreenToClient
Converts the screen coordinates of a given point or rectangle on the display to client coordinates.  
  
## Syntax  
  
```  
  
      void ScreenToClient(  
   LPPOINT lpPoint   
) const;  
void ScreenToClient(  
   LPRECT lpRect   
) const;  
```  
  
#### Parameters  
 `lpPoint`  
 Points to a [CPoint](../vs140/CPoint-Class.md) object or [POINT](../vs140/POINT-Structure.md) structure that contains the screen coordinates to be converted.  
  
 `lpRect`  
 Points to a [CRect](../vs140/CRect-Class.md) object or [RECT](../vs140/RECT-Structure.md) structure that contains the screen coordinates to be converted.  
  
## Remarks  
 The `ScreenToClient` member function replaces the screen coordinates given in `lpPoint` or `lpRect` with client coordinates. The new coordinates are relative to the upper-left corner of the `CWnd` client area.  
  
## Example  
 See the example for [CListCtrl::GetItemRect](../vs140/CListCtrl--GetItemRect.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::ClientToScreen](../vs140/CWnd--ClientToScreen.md)   
 [ScreenToClient](http://msdn.microsoft.com/library/windows/desktop/dd162952)