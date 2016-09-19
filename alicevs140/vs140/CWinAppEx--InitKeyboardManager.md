---
title: "CWinAppEx::InitKeyboardManager"
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
ms.assetid: e2b055c5-35a6-40ae-a21a-39cc9a7ab81a
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinAppEx::InitKeyboardManager
Initializes the [CKeyboardManager](../vs140/CKeyboardManager-Class.md) object.  
  
## Syntax  
  
```  
BOOL InitKeyboardManager();  
```  
  
## Return Value  
 Nonzero if the method creates the `CKeyboardManager` object; 0 if the `CKeyboardManager` object already exists.  
  
## Remarks  
 If you call [CWinAppEx::GetKeyboardManager](../vs140/CWinAppEx--GetKeyboardManager.md), the default implementation of that method calls `InitKeyboardManager`.  
  
 If your application already has a keyboard manager and you call `InitKeyboardManager`, your application will have an [ASSERT](../vs140/ASSERT--MFC-.md) failure. Therefore, you should not call `InitKeyboardManager` if you create a `CKeyboardManager` object directly. If you are not using a custom `CKeyboardManager`, you should use `GetKeyboardManager` to create a `CKeyboardManager` object.  
  
## Requirements  
 **Header:** afxwinappex.h  
  
## See Also  
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CWinAppEx::GetKeyboardManager](../vs140/CWinAppEx--GetKeyboardManager.md)   
 [CKeyboardManager Class](../vs140/CKeyboardManager-Class.md)