---
title: "CMFCPopupMenu::GetAnimationSpeed"
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
ms.assetid: aa319389-ede5-4e7e-911c-0b127990aa8c
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPopupMenu::GetAnimationSpeed
Returns the animation speed for pop-up menus.  
  
## Syntax  
  
```  
static UINT GetAnimationSpeed();  
```  
  
## Return Value  
 An integer that indicates the time, in milliseconds, that a pop-up menu animation takes to finish.  
  
## Remarks  
 The animation speed is a global value. Use [CMFCPopupMenu::SetAnimationSpeed](../vs140/CMFCPopupMenu--SetAnimationSpeed.md) to change the animation speed for pop-up menus.  
  
## Requirements  
 **Header:** afxpopupmenu.h  
  
## See Also  
 [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCPopupMenu::SetAnimationSpeed](../vs140/CMFCPopupMenu--SetAnimationSpeed.md)