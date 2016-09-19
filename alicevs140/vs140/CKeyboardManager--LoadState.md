---
title: "CKeyboardManager::LoadState"
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
ms.assetid: 705d02bc-19fd-4451-84a8-845ddeead02a
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CKeyboardManager::LoadState
Loads the shortcut key tables from the Windows registry.  
  
## Syntax  
  
```  
BOOL LoadState(  
   LPCTSTR lpszProfileName = NULL,  
   CFrameWnd* pDefaultFrame = NULL  
);  
```  
  
#### Parameters  
 [in] `lpszProfileName`  
 The registry path where `CKeyboardManager` data is saved.  
  
 [in] `pDefaultFrame`  
 A pointer to a frame window to use as the default window.  
  
## Return Value  
 Nonzero if the state was loaded successfully or 0 otherwise.  
  
## Remarks  
 If the `lpszProfileName` parameter is `NULL`, this method checks the default registry location for `CKeyboardManager` data. The default registry location is specified by the [CWinAppEx Class](../vs140/CWinAppEx-Class.md). The data must be previously written with the method [CKeyboardManager::SaveState](../vs140/CKeyboardManager--SaveState.md).  
  
 If you do not specify a default window, the main frame window of your application will be used.  
  
## Requirements  
 **Header:** afxkeyboardmanager.h  
  
## See Also  
 [CKeyboardManager Class](../vs140/CKeyboardManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [CKeyboardManager::SaveState](../vs140/CKeyboardManager--SaveState.md)