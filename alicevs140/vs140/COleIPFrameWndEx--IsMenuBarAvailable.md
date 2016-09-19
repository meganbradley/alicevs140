---
title: "COleIPFrameWndEx::IsMenuBarAvailable"
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
ms.assetid: 4353e73d-ae0e-4531-971e-3ac266771b09
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleIPFrameWndEx::IsMenuBarAvailable
Determines whether the pointer to the menu bar object is not `NULL`  
  
## Syntax  
  
```  
BOOL IsMenuBarAvailable() const;  
```  
  
## Return Value  
 Returns a non-zero value if the frame window has a menu bar; otherwise returns 0.  
  
## Remarks  
 Call this method to determine whether the frame window maintains a non-`NULL` pointer to its menu bar object.  
  
## Requirements  
 **Header:** afxoleipframewndex.h  
  
## See Also  
 [COleIPFrameWndEx Class](../vs140/COleIPFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)