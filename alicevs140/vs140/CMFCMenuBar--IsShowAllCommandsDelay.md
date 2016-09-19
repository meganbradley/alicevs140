---
title: "CMFCMenuBar::IsShowAllCommandsDelay"
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
ms.assetid: f4ac9d63-544c-476b-9347-482ebe9317cc
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCMenuBar::IsShowAllCommandsDelay
Indicates whether the [CMFCMenuBar](../vs140/CMFCMenuBar-Class.md) object displays all the commands after a short delay.  
  
## Syntax  
  
```  
static BOOL IsShowAllCommandsDelay();  
```  
  
## Return Value  
 Nonzero if the menu bar displays full menus after a short delay; otherwise 0.  
  
## Remarks  
 When you configure a menu bar to display recently used items, the menu bar displays the full menu in one of two ways:  
  
-   Display the full menu after a programmed delay from when the user hovers the cursor over the arrow at the bottom of the menu.  
  
-   Display the full menu after the user clicks the arrow at the bottom of the menu.  
  
 By default, all `CMFCMenuBar` objects use the option to display the full menu after a short delay. This option cannot be changed programmatically in the `CMFCMenuBar` class. However, a user can change the behavior during toolbar customization by using the **Customize** dialog box..  
  
## Requirements  
 **Header:** afxmenubar.h  
  
## See Also  
 [CMFCMenuBar Class](../vs140/CMFCMenuBar-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)