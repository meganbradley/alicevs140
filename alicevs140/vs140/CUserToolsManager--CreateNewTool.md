---
title: "CUserToolsManager::CreateNewTool"
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
ms.assetid: 2f724fe3-632d-40c4-a3ed-4ad15218d6f3
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CUserToolsManager::CreateNewTool
Creates a new user tool.  
  
## Syntax  
  
```  
CUserTool* CreateNewTool();  
```  
  
## Return Value  
 A pointer to the newly created user tool, or `NULL` if the number of user tools has exceeded the maximum. The returned type is the same as the type that is passed to `CWinAppEx::EnableUserTools` as the `pToolRTC` parameter.  
  
## Remarks  
 This method finds the first available menu command ID in the range that is supplied in the call to [CWinAppEx::EnableUserTools](../vs140/CWinAppEx--EnableUserTools.md) and assigns the user tool this ID.  
  
 The method fails if the number of tools has reached the maximum. This occurs when all command IDs within the range are assigned to user tools. You can retrieve the maximum number of tools by calling [CUserToolsManager::GetMaxTools](../vs140/CUserToolsManager--GetMaxTools.md). You can get access to the tools list by calling the [CUserToolsManager::GetUserTools](../vs140/CUserToolsManager--GetUserTools.md) method.  
  
## Requirements  
 **Header:** afxusertoolsmanager.h  
  
## See Also  
 [CUserToolsManager Class](../vs140/CUserToolsManager-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)