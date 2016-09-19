---
title: "CSplitterWnd::SplitRow"
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
ms.assetid: c89dc71a-0f78-40fb-a106-319754b81f39
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSplitterWnd::SplitRow
Indicates where a frame window splits horizontally.  
  
## Syntax  
  
```  
  
      virtual BOOL SplitRow(  
   int cyBefore   
);  
```  
  
#### Parameters  
 *cyBefore*  
 The position, in pixels, before which the split occurs.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 This member function is called when a horizontal splitter window is created. `SplitRow` indicates the default location where the split occurs.  
  
 `SplitRow` is called by the framework to implement the logic of the dynamic splitter window (that is, if the splitter window has the **SPLS_DYNAMIC_SPLIT** style). It can be customized, along with the virtual function [CreateView](../vs140/CSplitterWnd--CreateView.md), to implement more advanced dynamic splitters.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CSplitterWnd Class](../vs140/CSplitterWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSplitterWnd::SplitColumn](../vs140/CSplitterWnd--SplitColumn.md)   
 [CSplitterWnd::CreateView](../vs140/CSplitterWnd--CreateView.md)   
 [CSplitterWnd::RecalcLayout](../vs140/CSplitterWnd--RecalcLayout.md)