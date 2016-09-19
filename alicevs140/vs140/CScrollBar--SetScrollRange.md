---
title: "CScrollBar::SetScrollRange"
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
ms.assetid: 5e10a0ac-9fdd-423c-9a9d-ab0481609b3a
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CScrollBar::SetScrollRange
Sets minimum and maximum position values for the given scroll bar.  
  
## Syntax  
  
```  
  
      void SetScrollRange(  
   int nMinPos,  
   int nMaxPos,  
   BOOL bRedraw = TRUE   
);  
```  
  
#### Parameters  
 `nMinPos`  
 Specifies the minimum scrolling position.  
  
 `nMaxPos`  
 Specifies the maximum scrolling position.  
  
 `bRedraw`  
 Specifies whether the scroll bar should be redrawn to reflect the change. If `bRedraw` is **TRUE**, the scroll bar is redrawn; if **FALSE**, it is not redrawn. It is redrawn by default.  
  
## Remarks  
 Set `nMinPos` and `nMaxPos` to 0 to hide standard scroll bars.  
  
 Do not call this function to hide a scroll bar while processing a scroll-bar notification message.  
  
 If a call to `SetScrollRange` immediately follows a call to the `SetScrollPos` member function, set `bRedraw` in `SetScrollPos` to 0 to prevent the scroll bar from being redrawn twice.  
  
 The difference between the values specified by `nMinPos` and `nMaxPos` must not be greater than 32,767. The default range for a scroll-bar control is empty (both `nMinPos` and `nMaxPos` are 0).  
  
## Example  
 [!CODE [NVC_MFC_CScrollBar#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CScrollBar#4)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CScrollBar Class](../vs140/CScrollBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CScrollBar::GetScrollPos](../vs140/CScrollBar--GetScrollPos.md)   
 [CScrollBar::SetScrollPos](../vs140/CScrollBar--SetScrollPos.md)   
 [CScrollBar::GetScrollRange](../vs140/CScrollBar--GetScrollRange.md)   
 [SetScrollRange](http://msdn.microsoft.com/library/windows/desktop/bb787599)