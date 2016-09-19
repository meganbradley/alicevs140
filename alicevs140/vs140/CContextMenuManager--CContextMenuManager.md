---
title: "CContextMenuManager::CContextMenuManager"
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
ms.assetid: 6eb3fc77-623f-4e5f-9c1d-3bf025813d4e
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CContextMenuManager::CContextMenuManager
Constructs a [CContextMenuManager](../vs140/CContextMenuManager-Class.md) object.  
  
## Syntax  
  
```  
CContextMenuManager();  
```  
  
## Remarks  
 In most cases, you should not create a `CContextMenuManager` manually. The framework of your application creates the `CContextMenuManager` object. You should call [CWinAppEx::InitContextMenuManager](../vs140/CWinAppEx--InitContextMenuManager.md) during the initialization of your application. To get a pointer to the context manager, call [CWinAppEx::GetContextMenuManager](../vs140/CWinAppEx--GetContextMenuManager.md).  
  
## Requirements  
 **Header:** afxcontextmenumanager.h  
  
## See Also  
 [CContextMenuManager Class](../vs140/CContextMenuManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)