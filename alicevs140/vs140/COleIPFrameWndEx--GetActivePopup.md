---
title: "COleIPFrameWndEx::GetActivePopup"
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
ms.assetid: 9258ad15-11e8-4298-b8ce-3bc84260d654
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleIPFrameWndEx::GetActivePopup
Returns a pointer to the currently displayed pop-up menu.  
  
## Syntax  
  
```  
CMFCPopupMenu* GetActivePopup() const;  
```  
  
## Return Value  
 A pointer to the active pop-up menu; otherwise `NULL`.  
  
## Remarks  
 Use this method to obtain a pointer to the [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md) object that is currently displayed.  
  
## Requirements  
 **Header:** afxoleipframewndex.h  
  
## See Also  
 [COleIPFrameWndEx Class](../vs140/COleIPFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)