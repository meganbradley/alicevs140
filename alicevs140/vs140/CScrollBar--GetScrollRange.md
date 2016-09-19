---
title: "CScrollBar::GetScrollRange"
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
ms.assetid: 000a4f4a-198f-4937-a71d-c8e920bc0564
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CScrollBar::GetScrollRange
Copies the current minimum and maximum scroll-bar positions for the given scroll bar to the locations specified by `lpMinPos` and `lpMaxPos`.  
  
## Syntax  
  
```  
  
      void GetScrollRange(  
   LPINT lpMinPos,  
   LPINT lpMaxPos   
) const;  
```  
  
#### Parameters  
 `lpMinPos`  
 Points to the integer variable that is to receive the minimum position.  
  
 `lpMaxPos`  
 Points to the integer variable that is to receive the maximum position.  
  
## Remarks  
 The default range for a scroll-bar control is empty (both values are 0).  
  
## Example  
 See the example for [CWnd::OnHScroll](../vs140/CWnd--OnHScroll.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CScrollBar Class](../vs140/CScrollBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [GetScrollRange](http://msdn.microsoft.com/library/windows/desktop/bb787587)   
 [CScrollBar::SetScrollRange](../vs140/CScrollBar--SetScrollRange.md)   
 [CScrollBar::GetScrollPos](../vs140/CScrollBar--GetScrollPos.md)   
 [CScrollBar::SetScrollPos](../vs140/CScrollBar--SetScrollPos.md)