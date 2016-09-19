---
title: "CMFCToolBar::AddBasicCommand"
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
ms.assetid: 1a484ca0-4a4e-4795-af28-9235dbcb903c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::AddBasicCommand
Adds a menu command to the list of commands that are always displayed when a user opens a menu.  
  
## Syntax  
  
```  
static void __stdcall AddBasicCommand(  
   UINT uiCmd   
);  
```  
  
#### Parameters  
 [in] `uiCmd`  
 Specifies the command to add.  
  
## Remarks  
 A basic command is always displayed when the menu is opened. This method is meaningful when the user chooses to view recently used commands.  
  
 Use the [CMFCToolBar::SetBasicCommands](../vs140/CMFCToolBar--SetBasicCommands.md) method to set the list of commands that are always displayed when a user opens a menu. Use the [CMFCToolBar::GetBasicCommands](../vs140/CMFCToolBar--GetBasicCommands.md) method to retrieve the list of basic commands that is used by your application.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBar::SetBasicCommands](../vs140/CMFCToolBar--SetBasicCommands.md)   
 [CMFCToolBar::GetBasicCommands](../vs140/CMFCToolBar--GetBasicCommands.md)