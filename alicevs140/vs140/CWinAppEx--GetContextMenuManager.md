---
title: "CWinAppEx::GetContextMenuManager"
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
ms.assetid: 31827311-4dbc-4da2-9d97-bb4189ae3f7f
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinAppEx::GetContextMenuManager
Returns a pointer to the global [CContextMenuManager](../vs140/CContextMenuManager-Class.md) object.  
  
## Syntax  
  
```  
CContextMenuManager* GetContextMenuManager();  
```  
  
## Return Value  
 A pointer to the global `CContextMenuManager` object.  
  
## Remarks  
 If the CContextMenuManager object is not initialized, this function calls [CWinAppEx::InitContextMenuManager](../vs140/CWinAppEx--InitContextMenuManager.md) before it returns a pointer.  
  
## Requirements  
 **Header:** afxwinappex.h  
  
## See Also  
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CWinAppEx::InitContextMenuManager](../vs140/CWinAppEx--InitContextMenuManager.md)   
 [CContextMenuManager Class](../vs140/CContextMenuManager-Class.md)