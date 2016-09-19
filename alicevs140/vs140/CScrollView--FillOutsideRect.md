---
title: "CScrollView::FillOutsideRect"
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
ms.assetid: 0d08195d-723b-4062-b4f3-c803a31de17a
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CScrollView::FillOutsideRect
Call `FillOutsideRect` to fill the area of the view that appears outside of the scrolling area.  
  
## Syntax  
  
```  
  
      void FillOutsideRect(  
   CDC* pDC,  
   CBrush* pBrush   
);  
```  
  
#### Parameters  
 `pDC`  
 Device context in which the filling is to be done.  
  
 `pBrush`  
 Brush with which the area is to be filled.  
  
## Remarks  
 Use `FillOutsideRect` in your scroll view's `OnEraseBkgnd` handler function to prevent excessive background repainting.  
  
## Example  
 [!CODE [NVC_MFCDocView#164](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#164)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CScrollView Class](../vs140/CScrollView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::OnEraseBkgnd](../vs140/CWnd--OnEraseBkgnd.md)