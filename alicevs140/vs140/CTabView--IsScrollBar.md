---
title: "CTabView::IsScrollBar"
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
ms.assetid: d0821a08-b609-49b5-9ad3-ba3c18055914
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTabView::IsScrollBar
Called by the framework when creating a tab view to determine whether the tab view has a shared horizontal scroll bar.  
  
## Syntax  
  
```  
virtual BOOL IsScrollBar() const;  
```  
  
## Return Value  
 `TRUE` if the tab view should be created together with a shared scroll bar. Otherwise, `FALSE`.  
  
## Remarks  
 The framework calls this method when a `CTabView` object is being created.  
  
 Override the `IsScrollBar` method in a `CTabView`-derived class and return `TRUE` if you want to create a view that has a shared horizontal scroll bar.  
  
## Requirements  
 **Header:** afxTabView.h  
  
## See Also  
 [CTabView Class](../vs140/CTabView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)