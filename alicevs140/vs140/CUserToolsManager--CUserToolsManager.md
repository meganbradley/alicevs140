---
title: "CUserToolsManager::CUserToolsManager"
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
ms.assetid: 7254bb70-d3e0-4dbd-a62d-e34c2866415e
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CUserToolsManager::CUserToolsManager
Constructs a `CUserToolsManager`. Each application must have at most one user tools manager.  
  
## Syntax  
  
```  
CUserToolsManager();  
CUserToolsManager(  
   const UINT uiCmdToolsDummy,  
   const UINT uiCmdFirst,  
   const UINT uiCmdLast,  
   CRuntimeClass* pToolRTC=RUNTIME_CLASS(CUserTool),  
   UINT uArgMenuID=0,  
   UINT uInitDirMenuID=0   
);  
```  
  
#### Parameters  
 [in] `uiCmdToolsDummy`  
 An unsigned integer that the framework uses as a placeholder for the command ID of the user tools menu.  
  
 [in] `uiCmdFirst`  
 The command ID for the first user tool command.  
  
 [in] `uiCmdLast`  
 The command ID for the last user tool command.  
  
 [in] `pToolRTC`  
 The class that [CUserToolsManager::CreateNewTool](../vs140/CUserToolsManager--CreateNewTool.md) creates. By using this class, you can use a derived type of [CUserTool](../vs140/CUserTool-Class.md) instead of the default implementation.  
  
 [in] `uArgMenuID`  
 The menu resource ID of the arguments popup menu.  
  
 [in] `uInitDirMenuID`  
 The menu resource ID of the initial directory popup menu.  
  
## Remarks  
 Do not call this constructor. Instead, call [CWinAppEx::EnableUserTools](../vs140/CWinAppEx--EnableUserTools.md) to enable user tools, and call [CWinAppEx::GetUserToolsManager](../vs140/CWinAppEx--GetUserToolsManager.md) to obtain a pointer to the `CUserToolsManager`. For more information, see [User Defined Tools](../vs140/User-defined-Tools.md).  
  
## Requirements  
 **Header:** afxusertoolsmanager.h  
  
## See Also  
 [CUserToolsManager Class](../vs140/CUserToolsManager-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)