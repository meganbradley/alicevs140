---
title: "CMFCSpinButtonCtrl::OnDraw"
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
ms.assetid: 9ba5ac21-9cd6-45b8-bf25-c8e5ff697030
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCSpinButtonCtrl::OnDraw
Repaints the current spin button control.  
  
## Syntax  
  
```  
virtual void OnDraw(  
   CDC* pDC  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
## Remarks  
 The framework calls the `CMFCSpinButtonCtrl::OnPaint` method to handle the [WM_PAINT](../vs140/CWnd--OnPaint.md) message, and that method in turn calls this `CMFCSpinButtonCtrl::OnDraw` method. Override this method to customize the way the framework draws the spin button control.  
  
## Requirements  
 **Header:** afxspinbuttonctrl.h  
  
## See Also  
 [CMFCSpinButtonCtrl Class](../vs140/CMFCSpinButtonCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CDC Class](../vs140/CDC-Class.md)   
 [CWnd::OnPaint](../vs140/CWnd--OnPaint.md)