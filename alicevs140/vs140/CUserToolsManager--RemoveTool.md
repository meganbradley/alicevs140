---
title: "CUserToolsManager::RemoveTool"
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
ms.assetid: c57dcbe8-5a9e-4178-afde-fb5ae9cd6a23
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CUserToolsManager::RemoveTool
Removes the specified user tool from the application.  
  
## Syntax  
  
```  
BOOL RemoveTool(  
   CUserTool* pTool   
);  
```  
  
#### Parameters  
 [in, out] `pTool`  
 A pointer to a user tool to be removed.  
  
## Return Value  
 `TRUE` if the tool is successfully removed. Otherwise, `FALSE`.  
  
## Remarks  
 If the tool is successfully removed, this method deletes `pTool`.  
  
## Requirements  
 **Header:** afxusertoolsmanager.h  
  
## See Also  
 [CUserToolsManager Class](../vs140/CUserToolsManager-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)