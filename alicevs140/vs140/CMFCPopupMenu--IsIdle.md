---
title: "CMFCPopupMenu::IsIdle"
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
ms.assetid: 46072f0c-8f7f-4efb-9910-23f605c95c9c
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPopupMenu::IsIdle
Indicates whether a pop-up menu is currently idle.  
  
## Syntax  
  
```  
virtual BOOL IsIdle() const;  
```  
  
## Return Value  
 `TRUE` if the pop-up menu is in idle mode; otherwise `FALSE`.  
  
## Remarks  
 By default, a pop-up menu is in idle mode if the display animation is complete and the user is not scrolling the pop-up menu.  
  
## Requirements  
 **Header:** afxpopupmenu.h  
  
## See Also  
 [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)