---
title: "CSplitterWndEx::OnDrawSplitter"
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
ms.assetid: 77b4a2e8-4fef-45c1-98ea-dfaaae3859a1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSplitterWndEx::OnDrawSplitter
Called by the framework to draw a splitter window.  
  
## Syntax  
  
```  
virtual void OnDrawSplitter(  
   CDC* pDC,  
   ESplitType nType,  
   const CRect& rect   
);  
```  
  
#### Parameters  
 [in] `pDC`  
 Pointer to the device context. If this parameter is `NULL`, the framework redraws the active window.  
  
 [in] `nType`  
 One of the `CSplitterWnd::ESplitType` enumeration values that specifies the splitter window element to draw. Valid values are `splitBox`, `splitBar`, `splitIntersection`, and `splitBorder`.  
  
 [in] `rect`  
 A bounding rectangle that specifies the dimensions and location to draw the specified splitter window element.  
  
## Remarks  
  
## Requirements  
 **Header:** afxsplitterwndex.h  
  
## See Also  
 [CSplitterWndEx Class](../vs140/CSplitterWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)