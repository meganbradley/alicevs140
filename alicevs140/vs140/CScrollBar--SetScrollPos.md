---
title: "CScrollBar::SetScrollPos"
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
ms.assetid: ee09abec-3bda-4626-9b79-6da4c74714a5
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CScrollBar::SetScrollPos
Sets the current position of a scroll box to that specified by `nPos` and, if specified, redraws the scroll bar to reflect the new position.  
  
## Syntax  
  
```  
  
      int SetScrollPos(  
   int nPos,  
   BOOL bRedraw = TRUE   
);  
```  
  
#### Parameters  
 `nPos`  
 Specifies the new position for the scroll box. It must be within the scrolling range.  
  
 `bRedraw`  
 Specifies whether the scroll bar should be redrawn to reflect the new position. If `bRedraw` is **TRUE**, the scroll bar is redrawn. If it is **FALSE**, it is not redrawn. The scroll bar is redrawn by default.  
  
## Return Value  
 Specifies the previous position of the scroll box if successful; otherwise 0.  
  
## Remarks  
 Set `bRedraw` to **FALSE** whenever the scroll bar will be redrawn by a subsequent call to another function to avoid having the scroll bar redrawn twice within a short interval.  
  
## Example  
 See the example for [CScrollBar::SetScrollRange](../vs140/CScrollBar--SetScrollRange.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CScrollBar Class](../vs140/CScrollBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CScrollBar::GetScrollPos](../vs140/CScrollBar--GetScrollPos.md)   
 [CScrollBar::GetScrollRange](../vs140/CScrollBar--GetScrollRange.md)   
 [CScrollBar::SetScrollRange](../vs140/CScrollBar--SetScrollRange.md)   
 [SetScrollPos](http://msdn.microsoft.com/library/windows/desktop/bb787597)