---
title: "CUserToolsManager::IsUserToolCmd"
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
ms.assetid: 186ada16-f9e8-40bf-8942-c3013aa5c3ec
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CUserToolsManager::IsUserToolCmd
Determines whether a command ID is associated with a user tool.  
  
## Syntax  
  
```  
BOOL IsUserToolCmd(  
   UINT uiCmdId   
) const;  
```  
  
#### Parameters  
 [in] `uiCmdId`  
 A command ID of the menu item.  
  
## Return Value  
 Nonzero if a given command ID is associated with a user tool; otherwise 0.  
  
## Remarks  
 This method checks whether the given command ID is in the command ID range. You specify the range when you call [CWinAppEx::EnableUserTools](../vs140/CWinAppEx--EnableUserTools.md) to enable user tools.  
  
## Requirements  
 **Header:** afxusertoolsmanager.h  
  
## See Also  
 [CUserToolsManager Class](../vs140/CUserToolsManager-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)