---
title: "CUserToolsManager::FindTool"
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
ms.assetid: 885a2620-39e1-4166-952f-b69afb3f6d84
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CUserToolsManager::FindTool
Returns the pointer to the [CUserTool Class](../vs140/CUserTool-Class.md) object that is associated with a specified command ID.  
  
## Syntax  
  
```  
CUserTool* FindTool(  
   UINT uiCmdId   
) const;  
```  
  
#### Parameters  
 [in] `uiCmdId`  
 A menu command identifier.  
  
## Return Value  
 A pointer to a [CUserTool Class](../vs140/CUserTool-Class.md) or `CUserTool`-derived object if success; otherwise `NULL`.  
  
## Remarks  
 When `FindTool` is successful, the returned type is the same as the type of the `pToolRTC` parameter to [CWinAppEx::EnableUserTools](../vs140/CWinAppEx--EnableUserTools.md).  
  
## Requirements  
 **Header:** afxusertoolsmanager.h  
  
## See Also  
 [CUserToolsManager Class](../vs140/CUserToolsManager-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)