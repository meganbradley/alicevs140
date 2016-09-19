---
title: "CUserToolsManager::MoveToolDown"
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
ms.assetid: 6b222100-905e-45c1-959f-6e63e699d822
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CUserToolsManager::MoveToolDown
Moves the specified user tool down in the list of user tools.  
  
## Syntax  
  
```  
BOOL MoveToolDown(  
   CUserTool* pTool   
);  
```  
  
#### Parameters  
 [in] `pTool`  
 Specifies the user tool to move.  
  
## Return Value  
 Nonzero if the user tool was moved down successfully; otherwise 0.  
  
## Remarks  
 The method fails if the tool that the `pTool` specifies is not in the internal list or if the tool is last in the list.  
  
## Requirements  
 **Header:** afxusertoolsmanager.h  
  
## See Also  
 [CUserToolsManager Class](../vs140/CUserToolsManager-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)