---
title: "CDataRecoveryHandler::SaveOpenDocumentList"
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
ms.assetid: 9be4bb86-ee22-46ec-be7c-eb078626fb47
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDataRecoveryHandler::SaveOpenDocumentList
Saves the current list of open documents to the Windows registry.  
  
## Syntax  
  
```  
virtual BOOL SaveOpenDocumentList();  
```  
  
## Return Value  
 `TRUE` if there are no open documents to save or if they were saved successfully. `FALSE` if there are documents to save to the registry, but they were not saved because an error occurred.  
  
## Remarks  
 The restart manager calls `SaveOpenDocumentList` when the application exits unexpectedly or when it exits for an upgrade. When the application restarts, it uses [CDataRecoveryHandler::ReadOpenDocumentList](../vs140/CDataRecoveryHandler--ReadOpenDocumentList.md) to retrieve the list of open documents.  
  
 This method saves only the list of open documents. The method [CDataRecoveryHandler::AutosaveDocumentInfo](../vs140/CDataRecoveryHandler--AutosaveDocumentInfo.md) is responsible for saving the documents themselves.  
  
## Requirements  
 **Header:** afxdatarecovery.h  
  
## See Also  
 [CDataRecoveryHandler Class](../vs140/CDataRecoveryHandler-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDataRecoveryHandler::ReadOpenDocumentList](../vs140/CDataRecoveryHandler--ReadOpenDocumentList.md)   
 [CDataRecoveryHandler::AutosaveDocumentInfo](../vs140/CDataRecoveryHandler--AutosaveDocumentInfo.md)