---
title: "CContextMenuManager::LoadState"
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
ms.assetid: 9f57090f-3a1f-46c0-88bf-808267d4dd41
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CContextMenuManager::LoadState
Loads information associated with the [CContextMenuManager Class](../vs140/CContextMenuManager-Class.md) from the Windows registry.  
  
## Syntax  
  
```  
virtual BOOL LoadState(  
   LPCTSTR lpszProfileName = NULL  
);  
```  
  
#### Parameters  
 [in] `lpszProfileName`  
 A string that contains the relative path of a registry key.  
  
## Return Value  
 Nonzero if the method is successful; otherwise 0.  
  
## Remarks  
 The `lpszProfileName` parameter is not the absolute path for a registry entry. It is a relative path that is added to the end of the default registry key for your application. To get or set the default registry key, use the methods [CWinAppEx::GetRegistryBase](../vs140/CWinAppEx--GetRegistryBase.md) and [CWinAppEx::SetRegistryBase](../vs140/CWinAppEx--SetRegistryBase.md) respectively.  
  
 Use the method [CContextMenuManager::SaveState](../vs140/CContextMenuManager--SaveState.md) to save the shortcut menus to the registry.  
  
## Requirements  
 **Header:** afxcontextmenumanager.h  
  
## See Also  
 [CContextMenuManager Class](../vs140/CContextMenuManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CContextMenuManager::SaveState](../vs140/CContextMenuManager--SaveState.md)