---
title: "CScrollBar::ShowScrollBar"
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
ms.assetid: 15d7b7b1-8b07-4316-baf4-1da2a1c1ebed
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CScrollBar::ShowScrollBar
Shows or hides a scroll bar.  
  
## Syntax  
  
```  
  
      void ShowScrollBar(  
   BOOL bShow = TRUE   
);  
```  
  
#### Parameters  
 `bShow`  
 Specifies whether the scroll bar is shown or hidden. If this parameter is **TRUE**, the scroll bar is shown; otherwise it is hidden.  
  
## Remarks  
 An application should not call this function to hide a scroll bar while processing a scroll-bar notification message.  
  
## Example  
 See the example for [CScrollBar::Create](../vs140/CScrollBar--Create.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CScrollBar Class](../vs140/CScrollBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CScrollBar::GetScrollPos](../vs140/CScrollBar--GetScrollPos.md)   
 [CScrollBar::GetScrollRange](../vs140/CScrollBar--GetScrollRange.md)   
 [CWnd::ScrollWindow](../vs140/CWnd--ScrollWindow.md)   
 [CScrollBar::SetScrollPos](../vs140/CScrollBar--SetScrollPos.md)   
 [CScrollBar::SetScrollRange](../vs140/CScrollBar--SetScrollRange.md)