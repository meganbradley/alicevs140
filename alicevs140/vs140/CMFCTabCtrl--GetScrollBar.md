---
title: "CMFCTabCtrl::GetScrollBar"
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
ms.assetid: 52c2af93-9a42-418d-9960-302c4fd47ea0
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTabCtrl::GetScrollBar
Retrieves a pointer to the scroll bar object that is associated with the tab control.  
  
## Syntax  
  
```  
CScrollBar* GetScrollBar();  
```  
  
## Return Value  
 A pointer to a scrollbar object, or a `NULL` if the tab control was not created by using the `STYLE_FLAT_SHARED_HORZ_SCROLL` style.  
  
## Remarks  
 Use this method to access the tab control's embedded scroll bar. A scroll bar object is created only when the tab control has the `STYLE_FLAT_SHARED_HORZ_SCROLL` style.  
  
## Requirements  
 **Header:** afxtabctrl.h  
  
## See Also  
 [CMFCTabCtrl Class](../vs140/CMFCTabCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CScrollBar Class](../vs140/CScrollBar-Class.md)