---
title: "CView::CView"
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
ms.assetid: 62c52836-1dd5-4cbd-a205-b4756e5b8a80
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CView::CView
Constructs a `CView` object.  
  
## Syntax  
  
```  
  
CView( );  
```  
  
## Remarks  
 The framework calls the constructor when a new frame window is created or a window is split. Override the [OnInitialUpdate](../vs140/CView--OnInitialUpdate.md) member function to initialize the view after the document is attached.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CView Class](../vs140/CView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CView::OnInitialUpdate](../vs140/CView--OnInitialUpdate.md)