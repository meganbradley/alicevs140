---
title: "CDataRecoveryHandler::RestoreAutosavedDocuments"
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
ms.assetid: 67046a50-6b6f-4111-99f4-47e7fbc48934
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDataRecoveryHandler::RestoreAutosavedDocuments
Restores the autosaved documents based on user input.  
  
## Syntax  
  
```  
virtual BOOL RestoreAutosavedDocuments();  
```  
  
## Return Value  
 `TRUE` if this method successfully restores the documents.  
  
## Remarks  
 This method calls [CDataRecoveryHandler::QueryRestoreAutosavedDocuments](../vs140/CDataRecoveryHandler--QueryRestoreAutosavedDocuments.md) to determine which documents the user wants to restore. If a user decides not to restore an autosaved document, `RestoreAutosavedDocuments` deletes the autosave file. Otherwise, `RestoreAutosavedDocuments` replaces the open document with the autosaved version.  
  
 To use this method, either `AFX_RESTART_MANAGER_REOPEN_PREVIOUS_FILES` or `AFX_RESTART_MANAGER_RESTORE_AUTOSAVED_FILES` must be set in `m_dwRestartManagerSupportFlags`. See [CDataRecoveryHandler Class](../vs140/CDataRecoveryHandler-Class.md) for more information about the `m_dwRestartManagerSupportFlags` parameter.  
  
## Requirements  
 **Header:** afxdatarecovery.h  
  
## See Also  
 [CDataRecoveryHandler Class](../vs140/CDataRecoveryHandler-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDataRecoveryHandler::ReopenPreviousDocuments](../vs140/CDataRecoveryHandler--ReopenPreviousDocuments.md)   
 [CDataRecoveryHandler::QueryRestoreAutosavedDocuments](../vs140/CDataRecoveryHandler--QueryRestoreAutosavedDocuments.md)