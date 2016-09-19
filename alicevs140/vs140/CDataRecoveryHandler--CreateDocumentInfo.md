---
title: "CDataRecoveryHandler::CreateDocumentInfo"
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
ms.assetid: 8e74a5cb-018c-4572-acf0-6f57627eab75
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDataRecoveryHandler::CreateDocumentInfo
Adds a document to the list of open documents.  
  
## Syntax  
  
```  
virtual BOOL CreateDocumentInfo(  
   CDocument *pDocument  
);  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|[in] `pDocument`|A pointer to a `CDocument`. This method creates the document information for this `CDocument`.|  
  
## Return Value  
 The default implementation returns `TRUE`.  
  
## Remarks  
 This method checks if `pDocument` is already in the list of documents before it adds the document. If `pDocument` is already in the list, this method deletes the autosaved file associated with `pDocument`.  
  
 To use this method, either `AFX_RESTART_MANAGER_AUTOSAVE_AT_RESTART` or `AFX_RESTARTMANAGER_AUTOSAVE_AT_INTERVAL` must be set in `m_dwRestartManagerSupportFlags`. See [CDataRecoveryHandler Class](../vs140/CDataRecoveryHandler-Class.md) for more information about the `m_dwRestartManagerSupportFlags` parameter.  
  
## Requirements  
 **Header:** afxdatarecovery.h  
  
## See Also  
 [CDataRecoveryHandler Class](../vs140/CDataRecoveryHandler-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocument Class](../vs140/CDocument-Class.md)   
 [CDataRecoveryHandler::UpdateDocumentInfo](../vs140/CDataRecoveryHandler--UpdateDocumentInfo.md)   
 [CDataRecoveryHandler::RemoveDocumentInfo](../vs140/CDataRecoveryHandler--RemoveDocumentInfo.md)