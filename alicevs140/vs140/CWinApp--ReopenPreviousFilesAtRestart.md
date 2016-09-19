---
title: "CWinApp::ReopenPreviousFilesAtRestart"
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
ms.assetid: 475af835-12fb-4c49-8187-31c1473045cf
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::ReopenPreviousFilesAtRestart
Determines whether the restart manager reopens the files that were open when the application exited unexpectedly.  
  
## Syntax  
  
```  
virtual BOOL ReopenPreviousFilesAtRestart() const;  
```  
  
## Return Value  
 `TRUE` indicates the restart manager reopens the previously open files; `FALSE` indicates the restart manager does not.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::SupportsRestartManager](../vs140/CWinApp--SupportsRestartManager.md)   
 [CWinApp::SupportsApplicationRecovery](../vs140/CWinApp--SupportsApplicationRecovery.md)   
 [CWinApp::SupportsAutosaveAtRestart](../vs140/CWinApp--SupportsAutosaveAtRestart.md)   
 [CWinApp::SupportsAutosaveAtInterval](../vs140/CWinApp--SupportsAutosaveAtInterval.md)   
 [CWinApp::RestoreAutosavedFilesAtRestart](../vs140/CWinApp--RestoreAutosavedFilesAtRestart.md)