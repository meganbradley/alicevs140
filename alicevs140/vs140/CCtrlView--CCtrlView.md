---
title: "CCtrlView::CCtrlView"
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
ms.assetid: b2426fe8-80e5-42a4-9864-bd516b12849a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCtrlView::CCtrlView
Constructs a `CCtrlView` object.  
  
## Syntax  
  
```  
  
      CCtrlView(  
   LPCTSTR lpszClass,  
   DWORD dwStyle   
);  
```  
  
#### Parameters  
 `lpszClass`  
 Windows class name of the view class.  
  
 `dwStyle`  
 Style of the view class.  
  
## Remarks  
 The framework calls the constructor when a new frame window is created or a window is split. Override [CView::OnInitialUpdate](../vs140/CView--OnInitialUpdate.md) to initialize the view after the document is attached. Call [CWnd::Create](../vs140/CWnd--Create.md) or [CWnd::CreateEx](../vs140/CWnd--CreateEx.md) to create the Windows object.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CCtrlView Class](../vs140/CCtrlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::PreCreateWindow](../vs140/CWnd--PreCreateWindow.md)