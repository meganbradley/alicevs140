---
title: "CDataRecoveryHandler::RemoveDocumentInfo"
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
ms.assetid: abfe415d-5032-405c-8dd6-47d54695c4ac
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDataRecoveryHandler::RemoveDocumentInfo
Removes the supplied document from the open document list.  
  
## Syntax  
  
```  
virtual BOOL RemoveDocumentInfo(  
   CDocument *pDocument  
);  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|[in] `pDocument`|A pointer to the document to remove.|  
  
## Return Value  
 `TRUE` if `pDocument` was removed from the list; `FALSE` if an error occurred.  
  
## Remarks  
 When the user closes a document, the framework uses this method to remove it from the list of open documents.  
  
 If `RemoveDocumentInfo` cannot find `pDocument` in the list of open documents, it does nothing and returns `TRUE`.  
  
 To use this method, `AFX_RESTART_MANAGER_REOPEN_PREVIOUS_FILES` must be set in `m_dwRestartManagerSupportFlags`. See [CDataRecoveryHandler Class](../vs140/CDataRecoveryHandler-Class.md) for more information about the `m_dwRestartManagerSupportFlags` parameter.  
  
## Requirements  
 **Header:** afxdatarecovery.h  
  
## See Also  
 [CDataRecoveryHandler Class](../vs140/CDataRecoveryHandler-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDataRecoveryHandler::CreateDocumentInfo](../vs140/CDataRecoveryHandler--CreateDocumentInfo.md)   
 [CDataRecoveryHandler::UpdateDocumentInfo](../vs140/CDataRecoveryHandler--UpdateDocumentInfo.md)