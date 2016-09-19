---
title: "CMFCListCtrl::GetHeaderCtrl"
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
ms.assetid: f60dbad3-a5ba-43b6-85a9-ce23f2b1f4f5
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCListCtrl::GetHeaderCtrl
Returns a reference to the header control.  
  
## Syntax  
  
```  
virtual CMFCHeaderCtrl& GetHeaderCtrl();  
```  
  
## Return Value  
 A reference to the underlying [CMFCHeaderCtrl](../vs140/CMFCHeaderCtrl-Class.md) object.  
  
## Remarks  
 The header control for a list control is the window that contains the titles for the columns. It is usually positioned directly above the columns.  
  
## Requirements  
 **Header:** afxlistctrl.h  
  
## See Also  
 [CMFCListCtrl Class](../vs140/CMFCListCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCHeaderCtrl Class](../vs140/CMFCHeaderCtrl-Class.md)