---
title: "CSplitterWnd::OnDrawSplitter"
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
ms.assetid: c4b973c7-db3b-48e4-9acb-2e7d26930a7f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSplitterWnd::OnDrawSplitter
Renders an image of a split window.  
  
## Syntax  
  
```  
  
      virtual void OnDrawSplitter(  
   CDC* pDC,  
   ESplitType nType,  
   const CRect& rect   
);  
```  
  
#### Parameters  
 `pDC`  
 A pointer to the device context in which to draw. If `pDC` is **NULL**, then [CWnd::RedrawWindow](../vs140/CWnd--RedrawWindow.md) is called by the framework and no split window is drawn.  
  
 `nType`  
 A value of the **enum ESplitType**, which can be one of the following:  
  
-   **splitBox** The splitter drag box.  
  
-   `splitBar` The bar that appears between the two split windows.  
  
-   **splitIntersection** The intersection of the split windows. This element will not be called when running on Windows 95/98.  
  
-   **splitBorder** The split window borders.  
  
 `rect`  
 A reference to a [CRect](../vs140/CRect-Class.md) object specifying the size and shape of the split windows.  
  
## Remarks  
 This member function is called by the framework to draw and specify the exact characteristics of a splitter window. Override `OnDrawSplitter` for advanced customization of the imagery for the various graphical components of a splitter window. The default imagery is similar to the splitter in Microsoft Works for Windows or Microsoft Windows 95/98, in that the intersections of the splitter bars are blended together.  
  
 For more on dynamic splitter windows, see "Splitter Windows" in the article [Multiple Document Types, Views, and Frame Windows](../vs140/Multiple-Document-Types--Views--and-Frame-Windows.md), [Technical Note 29](../vs140/TN029--Splitter-Windows.md), and the [CSplitterWnd](../vs140/CSplitterWnd-Class.md) class overview.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CSplitterWnd Class](../vs140/CSplitterWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSplitterWnd::OnInvertTracker](../vs140/CSplitterWnd--OnInvertTracker.md)