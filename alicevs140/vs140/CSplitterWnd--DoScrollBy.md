---
title: "CSplitterWnd::DoScrollBy"
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
ms.assetid: 62436eae-fb5e-4404-870a-8bb894dfa104
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSplitterWnd::DoScrollBy
Scrolls split windows by a given number of pixels.  
  
## Syntax  
  
```  
  
      virtual BOOL DoScrollBy(  
   CView* pViewFrom,  
   CSize sizeScroll,  
   BOOL bDoScroll = TRUE   
);  
```  
  
#### Parameters  
 `pViewFrom`  
 A pointer to the view from which the scrolling message originates.  
  
 `sizeScroll`  
 Number of pixels to be scrolled horizontally and vertically.  
  
 bDoScroll  
 Determines whether the specified scrolling action occurs. If `bDoScroll` is **TRUE** (that is, if a child window exists, and if the split windows have a scroll range), then the specified scrolling action can take place; if `bDoScroll` is **FALSE** (that is, if no child window exists, or the split views have no scroll range), then scrolling does not occur.  
  
## Return Value  
 Nonzero if synchronized scrolling occurs; otherwise 0.  
  
## Remarks  
 This member function is called by the framework in response to a scroll message, to perform synchronized scrolling of the split windows by the amount, in pixels, indicated by `sizeScroll`. Positive values indicate scrolling down and to the right; negative values indicate scrolling up and to the left.  
  
 Override to require an action by the user before allowing scroll.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CSplitterWnd Class](../vs140/CSplitterWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSplitterWnd::DoScroll](../vs140/CSplitterWnd--DoScroll.md)   
 [CView::OnScroll](../vs140/CView--OnScroll.md)