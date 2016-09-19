---
title: "CSplitterWnd::DeleteView"
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
ms.assetid: c1ec51ab-1f3d-49e7-98b6-f756e7b7a089
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSplitterWnd::DeleteView
Deletes a view from the splitter window.  
  
## Syntax  
  
```  
  
      virtual void DeleteView(  
   int row,  
   int col   
);  
```  
  
#### Parameters  
 `row`  
 Specifies the splitter window row at which to delete the view.  
  
 `col`  
 Specifies the splitter window column at which to delete the view.  
  
## Remarks  
 If the active view is being deleted, the next view will become active. The default implementation assumes the view will auto delete in [PostNcDestroy](../vs140/CWnd--PostNcDestroy.md).  
  
 This member function is called by the framework to implement the logic of the dynamic splitter window (that is, if the splitter window has the **SPLS_DYNAMIC_SPLIT** style). It can be customized, along with the virtual function [CreateView](../vs140/CSplitterWnd--CreateView.md), to implement more advanced dynamic splitters.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CSplitterWnd Class](../vs140/CSplitterWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::PostNcDestroy](../vs140/CWnd--PostNcDestroy.md)   
 [CSplitterWnd::CreateView](../vs140/CSplitterWnd--CreateView.md)   
 [CSplitterWnd::DeleteColumn](../vs140/CSplitterWnd--DeleteColumn.md)   
 [CSplitterWnd::DeleteRow](../vs140/CSplitterWnd--DeleteRow.md)