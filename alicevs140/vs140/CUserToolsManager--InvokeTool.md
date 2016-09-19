---
title: "CUserToolsManager::InvokeTool"
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
ms.assetid: bf478284-06b1-4c64-97e0-a2ba194b70aa
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CUserToolsManager::InvokeTool
Executes an application associated with the user tool that has a specified command ID.  
  
## Syntax  
  
```  
BOOL InvokeTool(  
   UINT uiCmdId   
);  
```  
  
#### Parameters  
 [in] `uiCmdId`  
 The menu command ID associated with the user tool.  
  
## Return Value  
 Nonzero if the command associated with user tool was executed successfully; otherwise 0.  
  
## Remarks  
 Call this method to execute an application associated with the user tool that has the command ID specified by `uiCmdId`.  
  
## Requirements  
 **Header:** afxusertoolsmanager.h  
  
## See Also  
 [CUserToolsManager Class](../vs140/CUserToolsManager-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)