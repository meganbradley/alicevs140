---
title: "CWinApp::SupportsRestartManager"
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
ms.assetid: 80048c46-e95d-4538-adf1-fc1bc9c2b29a
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::SupportsRestartManager
Determines whether the application supports the restart manager.  
  
## Syntax  
  
```  
virtual BOOL SupportsRestartManager() const;  
```  
  
## Return Value  
 `TRUE` indicates the application supports the restart manager; `FALSE` indicates the application does not.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::SupportsApplicationRecovery](../vs140/CWinApp--SupportsApplicationRecovery.md)   
 [CWinApp::SupportsAutosaveAtRestart](../vs140/CWinApp--SupportsAutosaveAtRestart.md)   
 [CWinApp::SupportsAutosaveAtInterval](../vs140/CWinApp--SupportsAutosaveAtInterval.md)   
 [CWinApp::ReopenPreviousFilesAtRestart](../vs140/CWinApp--ReopenPreviousFilesAtRestart.md)   
 [CWinApp::RestoreAutosavedFilesAtRestart](../vs140/CWinApp--RestoreAutosavedFilesAtRestart.md)   
 [CDataRecoveryHandler Class](../vs140/CDataRecoveryHandler-Class.md)