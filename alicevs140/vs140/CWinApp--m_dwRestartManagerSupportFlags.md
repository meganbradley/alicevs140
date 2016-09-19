---
title: "CWinApp::m_dwRestartManagerSupportFlags"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: db3ecf08-98a2-4734-85a1-741875292ca9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::m_dwRestartManagerSupportFlags
Flags that determine how the restart manager behaves.  
  
## Syntax  
  
```  
DWORD m_dwRestartManagerSupportFlags;  
```  
  
## Remarks  
 To enable the restart manager, set `m_dwRestartManagerSupportFlags` to the behavior that you want. The following table shows the flags that are available.  
  
|||  
|-|-|  
|Flag|Description|  
|`AFX_RESTART_MANAGER_SUPPORT_RESTART`|The application is registered by using [CWinApp::RegisterWithRestartManager](../vs140/CWinApp--RegisterWithRestartManager.md). The restart manager is responsible for restarting the application if it unexpectedly exits.|  
|-   `AFX_RESTART_MANAGER_SUPPORT_RECOVERY`|The application is registered with the restart manager and the restart manager calls the recovery callback function when it restarts the application. The default recovery callback function is [CWinApp::ApplicationRecoveryCallback](../vs140/CWinApp--ApplicationRecoveryCallback.md).|  
|-   `AFX_RESTART_MANAGER_AUTOSAVE_AT_RESTART`|Autosave is enabled and the restart manager autosaves any open documents when the application restarts.|  
|-   `AFX_RESTART_MANAGER_AUTOSAVE_AT_INTERVAL`|Autosave is enabled and the restart manager autosaves any open documents at a regular interval. The interval is defined by [CWinApp::m_nAutosaveInterval](../vs140/CWinApp--m_nAutosaveInterval.md).|  
|-   `AFX_RESTART_MANAGER_REOPEN_PREVIOUS_FILES`|The restart manager opens previously open documents after restarting the application from an unexpected exit. The [CDataRecoveryHandler Class](../vs140/CDataRecoveryHandler-Class.md) handles storing the list of open documents and restoring them.|  
|-   `AFX_RESTART_MANAGER_RESTORE_AUTOSAVED_FILES`|The restart manager prompts the user to restore autosaved files after restarting the application. The `CDataRecoveryHandler` class queries the user.|  
|-   `AFX_RESTART_MANAGER_SUPPORT_NO_AUTOSAVE`|The union of `AFX_RESTART_MANAGER_SUPPORT_RESTART`, `AFX_RESTART_MANAGER_SUPPORT_RECOVER`, and `AFX_RESTART_MANAGER_REOPEN_PREVIOUS_FILES`.|  
|-   `AFX_RESTART_MANAGER_SUPPORT_ALL_ASPECTS`|The union of `AFX_RESTART_MANAGER_SUPPORT_NO_AUTOSAVE`, `AFX_RESTART_MANAGER_AUTOSAVE_AT_RESTART`, `AFX_RESTART_MANAGER_AUTOSAVE_AT_INTERVAL`, and `AFX_RESTART_MANAGER_RESTORE_AUTOSAVED_FILES`.|  
|-   `AFX_RESTART_MANAGER_SUPPORT_RESTART_ASPECTS`|The union of `AFX_RESTART_MANAGER_SUPPORT_RESTART`, `AFX_RESTART_MANAGER_AUTOSAVE_AT_RESTART`, `AFX_RESTART_MANAGER_REOPEN_PREVIOUS_FILES`, and `AFX_RESTART_MANAGER_RESTORE_AUTOSAVED_FILES`.|  
|-   `AFX_RESTART_MANAGER_SUPPORT_RECOVERY_ASPECTS`|The union of `AFX_RESTART_MANAGER_SUPPORT_RECOVERY`, `AFX_RESTART_MANAGER_AUTOSAVE_AT_INTERVAL`, `AFX_RESTART_MANAGER_REOPEN_PREVIOUS_FILES`, and `AFX_RESTART_MANAGER_RESTORE_AUTOSAVED_FILES`.|  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [How to: Add Restart Manager Support](../vs140/How-to--Add-Restart-Manager-Support.md)