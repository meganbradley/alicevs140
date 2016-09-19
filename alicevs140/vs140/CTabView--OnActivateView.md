---
title: "CTabView::OnActivateView"
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
ms.assetid: afc7e199-1132-41d0-b436-81bbd7976fb4
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTabView::OnActivateView
Called by the framework when the tab view is made active or inactive.  
  
## Syntax  
  
```  
virtual void OnActivateView(  
   CView* view  
);  
```  
  
#### Parameters  
 [in] `view`  
 A pointer to the view.  
  
## Remarks  
 The default implementation does nothing. Override this method in a `CTabView`-derived class to process this notification.  
  
## Requirements  
 **Header:** afxTabView.h  
  
## See Also  
 [CTabView Class](../vs140/CTabView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)