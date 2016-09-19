---
title: "CKeyboardManager::ShowAllAccelerators"
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
ms.assetid: 67835c6d-546f-483f-8ead-7537ce7a8bf1
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CKeyboardManager::ShowAllAccelerators
Shows all the shortcut keys associated with menu commands.  
  
## Syntax  
  
```  
static void ShowAllAccelerators(  
   BOOL bShowAll = TRUE,  
   LPCTSTR lpszDelimiter = _afxDefaultAcceleratorDelimiter  
);  
```  
  
#### Parameters  
 [in] `bShowAll`  
 If `true`, all the shortcut keys will be displayed. If `false`, only the first shortcut key will be displayed.  
  
 [in] `lpszDelimiter`  
 A string to insert between shortcut keys. This delimiter has no effect if only one shortcut key is displayed.  
  
## Remarks  
 By default, if a command has more than one shortcut key associated with it, only the first shortcut key will be shown. This function enables you to list all the shortcut keys associated with all commands.  
  
 The shortcut keys will be listed next to the command in the menu bar. If all the shortcut keys are displayed, the string provided by `lpszDelimiter` will separate individual shortcut keys.  
  
## Requirements  
 **Header:** afxkeyboardmanager.h  
  
## See Also  
 [CKeyboardManager Class](../vs140/CKeyboardManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)