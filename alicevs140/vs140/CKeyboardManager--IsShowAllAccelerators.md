---
title: "CKeyboardManager::IsShowAllAccelerators"
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
ms.assetid: 39530005-0ded-42c8-a580-6d4560296c4c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CKeyboardManager::IsShowAllAccelerators
Indicates whether menus show all the shortcut keys associated with menu commands or only the default shortcut keys.  
  
## Syntax  
  
```  
static BOOL IsShowAllAccelerators();  
```  
  
## Return Value  
 Nonzero if the application lists all the shortcut keys for menu commands; 0 if the application displays only default shortcut keys.  
  
## Remarks  
 The application lists the shortcut keys for menu commands in the menu bar. Use the function [CKeyboardManager::ShowAllAccelerators](../vs140/CKeyboardManager--ShowAllAccelerators.md) to control whether the application lists all the shortcut keys or just the default shortcut keys.  
  
## Requirements  
 **Header:** afxkeyboardmanager.h  
  
## See Also  
 [CKeyboardManager Class](../vs140/CKeyboardManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CKeyboardManager::ShowAllAccelerators](../vs140/CKeyboardManager--ShowAllAccelerators.md)