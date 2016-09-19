---
title: "CUserToolsManager::GetToolsEntryCmd"
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
ms.assetid: b8b6749c-2e6b-4ae8-89fe-6c59b704960b
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CUserToolsManager::GetToolsEntryCmd
Returns the command ID of the menu item placeholder for user tools.  
  
## Syntax  
  
```  
UINT GetToolsEntryCmd() const;  
```  
  
## Return Value  
 The command ID of the placeholder.  
  
## Remarks  
 To enable user tools, you call [CWinAppEx::EnableUserTools](../vs140/CWinAppEx--EnableUserTools.md). The `uiCmdToolsDummy` parameter specifies the command ID of the tools entry command. This method returns the tools entry command ID. Wherever that ID is used in a menu, it is replaced by the list of user tools when the menu appears.  
  
## Requirements  
 **Header:** afxusertoolsmanager.h  
  
## See Also  
 [CUserToolsManager Class](../vs140/CUserToolsManager-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)