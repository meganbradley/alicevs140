---
title: "CMFCPopupMenu::GetAnimationType"
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
ms.assetid: 03ca2fc9-fa86-4cd3-8fcb-f136ed41aa31
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPopupMenu::GetAnimationType
Returns the current type of pop-up animation.  
  
## Syntax  
  
```  
static CMFCPopupMenu::ANIMATION_TYPE GetAnimationType(  
   BOOL bNoSystem = FALSE  
);  
```  
  
#### Parameters  
 [in] `bNoSystem`  
 A Boolean parameter that indicates whether this method checks the global value. FALSE if you want this method to return the animation style for this instance of the [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md).  
  
## Return Value  
 An enumerated value that describes the animation type.  
  
## Remarks  
 The style of animation for pop-up menus is global for your application. Use [CMFCPopupMenu::SetAnimationType](../vs140/CMFCPopupMenu--SetAnimationType.md) to set the animation style.  
  
 The following table lists the possible animation types.  
  
 NO_ANIMATION  
 The pop-up menu is not animated and appears immediately.  
  
 UNFOLD  
 The framework reveals the pop-up menu from the upper-left corner to the lower right corner.  
  
 SLIDE  
 The pop-up menu moves from top to bottom.  
  
 FADE  
 The pop-up menu first appears transparent and gradually solidifies.  
  
## Requirements  
 **Header:** afxpopupmenu.h  
  
## See Also  
 [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCPopupMenu::SetAnimationType](../vs140/CMFCPopupMenu--SetAnimationType.md)