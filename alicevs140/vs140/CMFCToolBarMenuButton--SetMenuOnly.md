---
title: "CMFCToolBarMenuButton::SetMenuOnly"
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
ms.assetid: dd0adf3a-78cb-4301-913c-39a5ab533027
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarMenuButton::SetMenuOnly
Specifies whether the button is drawn as a menu button or a split button when it has both a valid command ID and a submenu.  
  
## Syntax  
  
```  
void SetMenuOnly(  
   BOOL bMenuOnly   
);  
```  
  
#### Parameters  
 [in] `bMenuOnly`  
 `TRUE` to show this button as a menu button when it has both a valid command ID and a submenu, `FALSE` to show this button as a split button when it has both a valid command ID and a submenu.  
  
## Remarks  
 Typically, when a toolbar menu button has both a submenu and a command ID, the menu appears to be a split button that has a main button and an attached down arrow button. If you call this method and `bMenuOnly` is `TRUE`, the button instead appears to be a single menu button with a down arrow in the button. When the user clicks the arrow in either mode, the submenu opens, and when the user clicks the non-arrow part of the button in either mode the framework executes the command .  
  
## Requirements  
 **Header:** afxtoolbarmenubutton.h  
  
## See Also  
 [CMFCToolBarMenuButton Class](../vs140/CMFCToolBarMenuButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)