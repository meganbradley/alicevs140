---
title: "CKeyboardManager::CKeyboardManager"
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
ms.assetid: d41ac465-d6e0-44eb-a745-d5ab9b9b20b5
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CKeyboardManager::CKeyboardManager
Constructs a `CKeyboardManager` object.  
  
## Syntax  
  
```  
CKeyboardManager();  
```  
  
## Remarks  
 In most cases, you do not have to create a `CKeyboardManager` directly. By default, the framework creates one for you. To get a pointer to the `CKeyboardManager`, call [CWinAppEx::GetKeyboardManager](../vs140/CWinAppEx--GetKeyboardManager.md). If you do create one manually, you must initialize it with the method [CWinAppEx::InitKeyboardManager](../vs140/CWinAppEx--InitKeyboardManager.md).  
  
## Requirements  
 **Header:** afxkeyboardmanager.h  
  
## See Also  
 [CKeyboardManager Class](../vs140/CKeyboardManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CWinAppEx::GetKeyboardManager](../vs140/CWinAppEx--GetKeyboardManager.md)   
 [CWinAppEx::InitKeyboardManager](../vs140/CWinAppEx--InitKeyboardManager.md)