---
title: "CMFCToolBar::SetBasicCommands"
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
ms.assetid: 832a60c9-c6b4-42e9-9fff-fd43b5074b77
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::SetBasicCommands
Sets the list of commands that are always displayed when a user opens a menu.  
  
## Syntax  
  
```  
static void __stdcall SetBasicCommands(  
   CList<UINT,UINT>& lstCommands   
);  
```  
  
#### Parameters  
 [in] `lstCommands`  
 A reference to a `CList` object that contains a collection of commands.  
  
## Remarks  
 A basic command is always displayed when the menu is opened. This method is meaningful when the user chooses to view recently used commands.  
  
 Use the [CMFCToolBar::AddBasicCommand](../vs140/CMFCToolBar--AddBasicCommand.md) method to add a command to the list of basic commands. Use the [CMFCToolBar::GetBasicCommands](../vs140/CMFCToolBar--GetBasicCommands.md) method to retrieve the list of basic commands that is used by your application.  
  
 See the Explorer sample for an example that uses this method.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBar::AddBasicCommand](../vs140/CMFCToolBar--AddBasicCommand.md)   
 [CMFCToolBar::GetBasicCommands](../vs140/CMFCToolBar--GetBasicCommands.md)