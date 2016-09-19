---
title: "CDataRecoveryHandler::QueryRestoreAutosavedDocuments"
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
ms.assetid: acdfe062-07d1-4a33-b84b-de19091c0355
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDataRecoveryHandler::QueryRestoreAutosavedDocuments
Displays a dialog box to the user for each document that the `CDataRecoveryHandler` autosaved. The dialog box determines whether the user wants to restore the autosaved document.  
  
## Syntax  
  
```  
virtual void QueryRestoreAutosavedDocuments();  
```  
  
## Remarks  
 If your application is Unicode, this method displays a [CTaskDialog](../vs140/CTaskDialog-Class.md) to the user. Otherwise, the framework uses [AfxMessageBox](../vs140/AfxMessageBox.md) to query the user.  
  
 After `QueryRestoreAutosavedDocuments` gathers all the responses from the user, it stores the information in the member variable `m_mapDocNameToRestoreBool`. This method does not restore the autosaved documents.  
  
## Requirements  
 **Header:** afxdatarecovery.h  
  
## See Also  
 [CDataRecoveryHandler Class](../vs140/CDataRecoveryHandler-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDataRecoveryHandler::ReopenPreviousDocuments](../vs140/CDataRecoveryHandler--ReopenPreviousDocuments.md)   
 [CDataRecoveryHandler::RestoreAutosavedDocuments](../vs140/CDataRecoveryHandler--RestoreAutosavedDocuments.md)