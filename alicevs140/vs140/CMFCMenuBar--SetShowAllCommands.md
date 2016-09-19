---
title: "CMFCMenuBar::SetShowAllCommands"
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
ms.assetid: 8e9ab84e-76ad-45c3-a015-5f5b546df040
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCMenuBar::SetShowAllCommands
Controls whether a menu shows all the available commands.  
  
## Syntax  
  
```  
static void SetShowAllCommands(  
   BOOL bShowAllCommands = TRUE  
);  
```  
  
#### Parameters  
 [in] `bShowAllCommands`  
 A Boolean parameter that specifies whether the pop-up menu shows all the menu commands.  
  
## Remarks  
 If a menu does not display all the menu commands, it hides the commands that are rarely used. For more information about displaying menu commands, see [CMFCMenuBar Class](../vs140/CMFCMenuBar-Class.md).  
  
## Requirements  
 **Header:** afxmenubar.h  
  
## See Also  
 [CMFCMenuBar Class](../vs140/CMFCMenuBar-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCMenuBar::IsShowAllCommands](../vs140/CMFCMenuBar--IsShowAllCommands.md)