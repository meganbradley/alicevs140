---
title: "CWinAppEx::GetKeyboardManager"
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
ms.assetid: cb76f49c-232d-4220-9a1f-55707d5bf2a7
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinAppEx::GetKeyboardManager
Returns a pointer to the global [CKeyboardManager](../vs140/CKeyboardManager-Class.md) object.  
  
## Syntax  
  
```  
CKeyboardManager* GetKeyboardManager();  
```  
  
## Return Value  
 A pointer to the global `CKeyboardManager` object.  
  
## Remarks  
 If the keyboard manager is not initialized, this function calls [CWinAppEx::InitKeyboardManager](../vs140/CWinAppEx--InitKeyboardManager.md) before it returns a pointer.  
  
## Requirements  
 **Header:** afxwinappex.h  
  
## See Also  
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CKeyboardManager Class](../vs140/CKeyboardManager-Class.md)   
 [CWinAppEx::InitKeyboardManager](../vs140/CWinAppEx--InitKeyboardManager.md)