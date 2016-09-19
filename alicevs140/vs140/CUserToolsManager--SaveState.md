---
title: "CUserToolsManager::SaveState"
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
ms.assetid: 12bea579-6799-4351-afdf-f036d16b1f91
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CUserToolsManager::SaveState
Stores information about user tools in the Windows registry.  
  
## Syntax  
  
```  
BOOL SaveState(  
   LPCTSTR lpszProfileName=NULL   
);  
```  
  
#### Parameters  
 [in] `lpszProfileName`  
 A path to the Windows registry key.  
  
## Return Value  
 Nonzero if the state was saved successfully; otherwise 0.  
  
## Remarks  
 The method stores the current state of the [CUserToolsManager Class](../vs140/CUserToolsManager-Class.md) object in the Windows registry.  
  
 Usually, you do not need to call this method directly, [CWinAppEx::SaveState](../vs140/CWinAppEx--SaveState.md) calls it automatically as a part of the workspace serialization process of the application.  
  
## Requirements  
 **Header:** afxusertoolsmanager.h  
  
## See Also  
 [CUserToolsManager Class](../vs140/CUserToolsManager-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)