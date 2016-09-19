---
title: "CMouseManager::SaveState"
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
ms.assetid: 424c4e1d-a5fd-4f2e-beee-08807f6f3696
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMouseManager::SaveState
Writes the state of the [CMouseManager Class](../vs140/CMouseManager-Class.md) to the registry.  
  
## Syntax  
  
```  
BOOL SaveState(  
   LPCTSTR lpszProfileName = NULL  
);  
```  
  
#### Parameters  
 [in] `lpszProfileName`  
 A path of a registry key.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 The state information written to the registry includes all registered views, view identifiers, and the associated commands. If the parameter `lpszProfileName` is `NULL`, this function writes the `CMouseManager` data to the default registry location controlled by the [CWinAppEx Class](../vs140/CWinAppEx-Class.md).  
  
 In most cases, you do not have to call this function directly. It is called as a part of the workspace serialization process. For more information about the workspace serialization process, see [CWinAppEx::SaveState](../vs140/CWinAppEx--SaveState.md).  
  
## Requirements  
 **Header:** afxmousemanager.h  
  
## See Also  
 [CMouseManager Class](../vs140/CMouseManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [CWinAppEx::SaveState](../vs140/CWinAppEx--SaveState.md)