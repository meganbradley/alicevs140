---
title: "CSplitterWnd::SplitColumn"
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
ms.assetid: 2d395dcf-2e3a-413b-b399-1722b102d16c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSplitterWnd::SplitColumn
Indicates where a frame window splits vertically.  
  
## Syntax  
  
```  
  
      virtual BOOL SplitColumn(  
   int cxBefore   
);  
```  
  
#### Parameters  
 *cxBefore*  
 The position, in pixels, before which the split occurs.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 This member function is called when a vertical splitter window is created. `SplitColumn` indicates the default location where the split occurs.  
  
 `SplitColumn` is called by the framework to implement the logic of the dynamic splitter window (that is, if the splitter window has the **SPLS_DYNAMIC_SPLIT** style). It can be customized, along with the virtual function [CreateView](../vs140/CSplitterWnd--CreateView.md), to implement more advanced dynamic splitters.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CSplitterWnd Class](../vs140/CSplitterWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSplitterWnd::CreateView](../vs140/CSplitterWnd--CreateView.md)   
 [CSplitterWnd::SplitRow](../vs140/CSplitterWnd--SplitRow.md)   
 [CSplitterWnd::RecalcLayout](../vs140/CSplitterWnd--RecalcLayout.md)