---
title: "CMFCBaseTabCtrl::FindTargetWnd"
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
ms.assetid: 89304325-abfe-4417-ab52-3a9d2e47b9ae
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::FindTargetWnd
Identifies the pane that contains a specified point.  
  
## Syntax  
  
```  
virtual CWnd* FindTargetWnd(  
   const CPoint& pt   
) = 0;  
```  
  
#### Parameters  
 [in] `pt`  
 A point that is defined by using client-area coordinates of the [CMFCBaseTabCtrl](../vs140/CMFCBaseTabCtrl-Class.md) object.  
  
## Return Value  
 A pointer to a [CWnd](../vs140/CWnd-Class.md) object if successful; otherwise `NULL`.  
  
## Remarks  
 In the `CMFCBaseTabCtrl` class, this method is a pure virtual function: you must implement it if you derive a class from `CMFCBaseTabCtrl`.  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)