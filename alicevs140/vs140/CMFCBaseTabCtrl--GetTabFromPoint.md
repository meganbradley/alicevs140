---
title: "CMFCBaseTabCtrl::GetTabFromPoint"
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
ms.assetid: 7c6fa916-205e-4ecc-824a-9beff60b43b2
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::GetTabFromPoint
Retrieves the tab that contains a specified point.  
  
## Syntax  
  
```  
virtual int GetTabFromPoint(  
   CPoint& pt  
) const;  
```  
  
#### Parameters  
 [in] `pt`  
 A point in client coordinates of the tab control.  
  
## Return Value  
 The index of the tab that contains `pt`; -1 if no tab contains `pt`.  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)