---
title: "CWinApp::SupportsApplicationRecovery"
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
ms.assetid: 9f07ecf1-4f52-4bee-a8ce-bb4dd0b49504
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::SupportsApplicationRecovery
Determines whether the restart manager recovers an application that exited unexpectedly.  
  
## Syntax  
  
```  
virtual BOOL SupportsApplicationRecovery() const;  
```  
  
## Return Value  
 `TRUE` indicates the restart manager recovers the application; `FALSE` indicates the restart manager does not.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::SupportsRestartManager](../vs140/CWinApp--SupportsRestartManager.md)   
 [CWinApp::SupportsAutosaveAtRestart](../vs140/CWinApp--SupportsAutosaveAtRestart.md)   
 [CWinApp::SupportsAutosaveAtInterval](../vs140/CWinApp--SupportsAutosaveAtInterval.md)   
 [CWinApp::ReopenPreviousFilesAtRestart](../vs140/CWinApp--ReopenPreviousFilesAtRestart.md)   
 [CWinApp::RestoreAutosavedFilesAtRestart](../vs140/CWinApp--RestoreAutosavedFilesAtRestart.md)