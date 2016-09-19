---
title: "CWinAppEx::InitContextMenuManager"
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
ms.assetid: c8e6f9c5-e995-4973-89fb-8660701e0fb5
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinAppEx::InitContextMenuManager
Initializes the [CContextMenuManager](../vs140/CContextMenuManager-Class.md) object.  
  
## Syntax  
  
```  
BOOL InitContextMenuManager();  
```  
  
## Return Value  
 Nonzero if the method creates the CContextMenuManager object; 0 if the `CContextMenuManager` object already exists.  
  
## Remarks  
 If you call [CWinAppEx::GetContextMenuManager](../vs140/CWinAppEx--GetContextMenuManager.md), the default implementation of that method calls `InitContextMenuManager`.  
  
 If your application already has a context menu manager and you call `InitContextMenuManager`, your application will have an [ASSERT](../vs140/ASSERT--MFC-.md) failure. Therefore, you should not call `InitContextMenuManager` if you create a `CContextMenuManager` object directly. If you are not using a custom `CContextMenuManager`, you should use `GetContextMenuManager` to create a `CContextMenuManager` object.  
  
## Requirements  
 **Header:** afxwinappex.h  
  
## See Also  
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CWinAppEx::GetContextMenuManager](../vs140/CWinAppEx--GetContextMenuManager.md)   
 [CContextMenuManager Class](../vs140/CContextMenuManager-Class.md)