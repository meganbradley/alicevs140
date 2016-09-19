---
title: "CDataRecoveryHandler::UpdateDocumentInfo"
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
ms.assetid: 8041d538-3091-4516-ad43-8b4611c3dfb6
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDataRecoveryHandler::UpdateDocumentInfo
Updates the information for a document because the user saved it.  
  
## Syntax  
  
```  
virtual BOOL UpdateDocumentInfo(  
   CDocument *pDocument  
);  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|[in] `pDocument`|A pointer to the saved document.|  
  
## Return Value  
 `TRUE` if this method deleted the autosaved document and updated the document information; `FALSE` if an error occurred.  
  
## Remarks  
 When a user saves a document, the application removes the autosaved file because it is no longer needed. `UpdateDocumentInfo` deletes the autosaved file by calling [CDataRecoveryHandler::RemoveDocumentInfo](../vs140/CDataRecoveryHandler--RemoveDocumentInfo.md). `UpdateDocumentInfo` then adds the information from `pDocument` to the list of currently open documents because `RemoveDocumentInfo` deletes that information, but the saved document is still open.  
  
 To use this method, `AFX_RESTART_MANAGER_REOPEN_PREVIOUS_FILES` must be set in `m_dwRestartManagerSupportFlags`. See [CDataRecoveryHandler Class](../vs140/CDataRecoveryHandler-Class.md) for more information about the `m_dwRestartManagerSupportFlags` parameter.  
  
## Requirements  
 **Header:** afxdatarecovery.h  
  
## See Also  
 [CDataRecoveryHandler Class](../vs140/CDataRecoveryHandler-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDataRecoveryHandler::RemoveDocumentInfo](../vs140/CDataRecoveryHandler--RemoveDocumentInfo.md)