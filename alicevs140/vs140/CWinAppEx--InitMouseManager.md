---
title: "CWinAppEx::InitMouseManager"
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
ms.assetid: 26c58cbe-c29e-45f0-827e-27332c599edc
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinAppEx::InitMouseManager
Initializes the [CMouseManager](../vs140/CMouseManager-Class.md) object.  
  
## Syntax  
  
```  
BOOL InitMouseManager();  
```  
  
## Return Value  
 Nonzero if the method creates the `CMouseManager` object; 0 if the `CMouseManager` object already exists.  
  
## Remarks  
 If you call [CWinAppEx::GetMouseManager](../vs140/CWinAppEx--GetMouseManager.md), the default implementation of that method calls `InitMouseManager`.  
  
 If your application already has a mouse manager and you call `InitMouseManager`, your application will have an [ASSERT](../vs140/ASSERT--MFC-.md) failure. Therefore you should not call `InitMouseManager` if you create a `CMouseManager` object directly. If you are not using a custom `CMouseManager`, you should use `GetMouseManager` to create a `CMouseManager` object.  
  
## Requirements  
 **Header:** afxwinappex.h  
  
## See Also  
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CWinAppEx::GetMouseManager](../vs140/CWinAppEx--GetMouseManager.md)   
 [CMouseManager Class](../vs140/CMouseManager-Class.md)