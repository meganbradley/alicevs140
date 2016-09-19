---
title: "CWinApp::RestoreAutosavedFilesAtRestart"
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
ms.assetid: 4a43dfec-96e8-4968-bab7-98cb6cf37e22
caps.latest.revision: 8
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::RestoreAutosavedFilesAtRestart
Determines whether the restart manager restores the autosaved files when it restarts the application.  
  
## Syntax  
  
```  
virtual BOOL RestoreAutosavedFilesAtRestart() const;  
```  
  
## Return Value  
 `TRUE` indicates the restart manager restores autosaved files; `FALSE` indicates the restart manager does not.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::SupportsRestartManager](../vs140/CWinApp--SupportsRestartManager.md)   
 [CWinApp::SupportsApplicationRecovery](../vs140/CWinApp--SupportsApplicationRecovery.md)   
 [CWinApp::SupportsAutosaveAtRestart](../vs140/CWinApp--SupportsAutosaveAtRestart.md)   
 [CWinApp::SupportsAutosaveAtInterval](../vs140/CWinApp--SupportsAutosaveAtInterval.md)   
 [CWinApp::ReopenPreviousFilesAtRestart](../vs140/CWinApp--ReopenPreviousFilesAtRestart.md)