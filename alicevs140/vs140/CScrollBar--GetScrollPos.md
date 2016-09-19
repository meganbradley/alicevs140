---
title: "CScrollBar::GetScrollPos"
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
ms.assetid: 1f9ee5cb-906b-4e42-b136-db0808c3d959
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CScrollBar::GetScrollPos
Retrieves the current position of a scroll box.  
  
## Syntax  
  
```  
  
int GetScrollPos( ) const;  
```  
  
## Return Value  
 Specifies the current position of the scroll box if successful; otherwise 0.  
  
## Remarks  
 The current position is a relative value that depends on the current scrolling range. For example, if the scrolling range is 100 to 200 and the scroll box is in the middle of the bar, the current position is 150.  
  
## Example  
 See the example for [CWnd::OnHScroll](../vs140/CWnd--OnHScroll.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CScrollBar Class](../vs140/CScrollBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CScrollBar::SetScrollPos](../vs140/CScrollBar--SetScrollPos.md)   
 [CScrollBar::GetScrollRange](../vs140/CScrollBar--GetScrollRange.md)   
 [CScrollBar::SetScrollRange](../vs140/CScrollBar--SetScrollRange.md)   
 [GetScrollPos](http://msdn.microsoft.com/library/windows/desktop/bb787585)