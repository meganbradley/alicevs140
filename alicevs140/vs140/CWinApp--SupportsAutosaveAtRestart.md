---
title: "CWinApp::SupportsAutosaveAtRestart"
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
ms.assetid: 43b3477d-be76-4d63-aa48-8ac80722056e
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::SupportsAutosaveAtRestart
Determines whether the restart manager autosaves any open documents when the application restarts.  
  
## Syntax  
  
```  
virtual BOOL SupportsAutosaveAtRestart() const;  
```  
  
## Return Value  
 `TRUE` indicates the restart manager autosaves open documents when the application restarts; `FALSE` indicates the restart manager does not.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::SupportsRestartManager](../vs140/CWinApp--SupportsRestartManager.md)   
 [CWinApp::SupportsApplicationRecovery](../vs140/CWinApp--SupportsApplicationRecovery.md)   
 [CWinApp::SupportsAutosaveAtInterval](../vs140/CWinApp--SupportsAutosaveAtInterval.md)   
 [CWinApp::ReopenPreviousFilesAtRestart](../vs140/CWinApp--ReopenPreviousFilesAtRestart.md)   
 [CWinApp::RestoreAutosavedFilesAtRestart](../vs140/CWinApp--RestoreAutosavedFilesAtRestart.md)