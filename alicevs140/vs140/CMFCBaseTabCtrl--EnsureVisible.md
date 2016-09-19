---
title: "CMFCBaseTabCtrl::EnsureVisible"
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
ms.assetid: 9957ddd9-e195-443c-ac0b-c64c9b86a761
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::EnsureVisible
Scrolls the tabs until the specified tab is visible.  
  
## Syntax  
  
```  
virtual BOOL EnsureVisible(  
   int iTab  
);  
```  
  
#### Parameters  
 [in] `iTab`  
 The zero-based index of a tab.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 This method has no effect if the tab indicated by `iTab` is already visible.  
  
 By default, this method is not supported by the [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md). You should implement this function in a custom class derived from `CMFCBaseTabCtrl` if that custom tab control supports tab scrolling. This method is supported by the [CMFCTabCtrl Class](../vs140/CMFCTabCtrl-Class.md).  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)