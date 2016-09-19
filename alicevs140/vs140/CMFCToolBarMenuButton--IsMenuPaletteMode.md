---
title: "CMFCToolBarMenuButton::IsMenuPaletteMode"
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
ms.assetid: d6d30237-da14-487c-8267-6140c9367206
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarMenuButton::IsMenuPaletteMode
Determines whether the drop-down menu is in palette mode.  
  
## Syntax  
  
```  
BOOL IsMenuPaletteMode() const;  
```  
  
## Return Value  
 `TRUE` if the palette mode is enabled, otherwise `FALSE`.  
  
## Remarks  
 When the menu button is set to palette mode, menu items appear in multiple columns with only a limited number of rows. Call this method to obtain the number of rows. You can enable or disable the palette mode by calling [CMFCToolBarMenuButton::SetMenuPaletteMode](../vs140/CMFCToolBarMenuButton--SetMenuPaletteMode.md).  
  
## Requirements  
 **Header:** afxtoolbarmenubutton.h  
  
## See Also  
 [CMFCToolBarMenuButton Class](../vs140/CMFCToolBarMenuButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)