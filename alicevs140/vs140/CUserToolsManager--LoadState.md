---
title: "CUserToolsManager::LoadState"
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
ms.assetid: 5f7ebcd3-48a8-4f1b-9935-c7b95f8a717c
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CUserToolsManager::LoadState
Loads information about user tools from the Windows registry.  
  
## Syntax  
  
```  
BOOL LoadState(  
   LPCTSTR lpszProfileName=NULL   
);  
```  
  
#### Parameters  
 [in] `lpszProfileName`  
 The path of the Windows registry key.  
  
## Return Value  
 Nonzero if the state was loaded successfully; otherwise 0.  
  
## Remarks  
 This method loads the state of the [CUserToolsManager Class](../vs140/CUserToolsManager-Class.md) object from the Windows registry.  
  
 Usually, you do not call this method directly. [CWinAppEx::LoadState](../vs140/CWinAppEx--LoadState.md) calls it as part of workspace initialization process.  
  
## Requirements  
 **Header:** afxusertoolsmanager.h  
  
## See Also  
 [CUserToolsManager Class](../vs140/CUserToolsManager-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)