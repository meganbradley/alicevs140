---
title: "CKeyboardManager::CleanUp"
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
ms.assetid: 53e84566-194d-4c3c-a23c-86948a7fd43c
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CKeyboardManager::CleanUp
Frees the `CKeyboardManager` resources and clears all shortcut key mappings.  
  
## Syntax  
  
```  
static void CleanUp();  
```  
  
## Remarks  
 For more information about shortcut keys, see [Keyboard and Mouse Customization](../vs140/Keyboard-and-Mouse-Customization.md).  
  
 You do not have to call this function when your application exits because the framework calls it automatically during application exit.  
  
## Requirements  
 **Header:** afxkeyboardmanager.h  
  
## See Also  
 [CKeyboardManager Class](../vs140/CKeyboardManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [Keyboard and Mouse Customization](../vs140/Keyboard-and-Mouse-Customization.md)   
 [CMFCAcceleratorKey Class](../vs140/CMFCAcceleratorKey-Class.md)   
 [CMFCAcceleratorKeyAssignCtrl Class](../vs140/CMFCAcceleratorKeyAssignCtrl-Class.md)