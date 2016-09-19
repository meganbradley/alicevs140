---
title: "CMFCTabCtrl::IsSharedScroll"
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
ms.assetid: e33d8e6c-ab19-4209-b506-3f83c40a4097
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTabCtrl::IsSharedScroll
Indicates whether the current tab control has a scroll bar that can scroll its tabs as a group.  
  
## Syntax  
  
```  
BOOL IsSharedScroll() const;  
```  
  
## Return Value  
 `TRUE` if the tab control has a shared scroll bar; otherwise, `FALSE`.  
  
## Remarks  
 This method returns `TRUE` if the `style` parameter of the [CMFCTabCtrl::Create](../vs140/CMFCTabCtrl--Create.md) method is STYLE_FLAT_SHARED_HORZ_SCROLL.  
  
## Requirements  
 **Header:** afxtabctrl.h  
  
## See Also  
 [CMFCTabCtrl Class](../vs140/CMFCTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCTabCtrl::Create](../vs140/CMFCTabCtrl--Create.md)