---
title: "CMFCBaseTabCtrl::GetTabArea"
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
ms.assetid: 3e3fa993-9f82-4ae0-909c-208b722f7735
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::GetTabArea
Retrieves the size and position of the tab area of the tab control.  
  
## Syntax  
  
```  
virtual void GetTabArea(  
   CRect& rectTabAreaTop,  
   CRect& rectTabAreaBottom  
) const = 0;  
```  
  
#### Parameters  
 [in] `rectTabAreaTop`  
 A reference to a `CRect` object. `GetTabArea` uses this object to store the size and position of the top tab area.  
  
 [in] `rectTabAreaBottom`  
 A reference to a `CRect` object. `GetTabArea` uses this object to store the size and position of the bottom tab area.  
  
## Remarks  
 After `GetTabArea` returns, the `CRect` parameters contain the size and position of the tab area in client coordinates of the tab control. If there is no tab area at the top or bottom of the tab control, `rectTabAreaTop` or `rectTabAreaBottom` are empty.  
  
 In the [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md), this method is a pure virtual function and has no implementation. If you derive a class from `CMFCBaseTabCtrl`, you have to implement this function.  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)