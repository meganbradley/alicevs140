---
title: "CView::OnDragLeave"
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
ms.assetid: 969e4208-c4f1-457d-b9c7-da93b25f76da
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CView::OnDragLeave
Called by the framework during a drag operation when the mouse is moved out of the valid drop area for that window.  
  
## Syntax  
  
```  
  
virtual void OnDragLeave( );  
```  
  
## Remarks  
 Override this function if the current view needs to clean up any actions taken during [OnDragEnter](../vs140/CView--OnDragEnter.md) or [OnDragOver](../vs140/CView--OnDragOver.md) calls, such as removing any visual user feedback while the object was dragged and dropped.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CView Class](../vs140/CView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CView::OnDragEnter](../vs140/CView--OnDragEnter.md)   
 [CView::OnDragOver](../vs140/CView--OnDragOver.md)   
 [CView::OnScroll](../vs140/CView--OnScroll.md)   
 [COleDropTarget::OnDragLeave](../vs140/COleDropTarget--OnDragLeave.md)