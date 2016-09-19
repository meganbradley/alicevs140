---
title: "CWinApp::SupportsAutosaveAtInterval"
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
ms.assetid: 26ac68e8-2a99-4257-ba49-427952900c1f
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::SupportsAutosaveAtInterval
Determines whether the restart manager autosaves open documents at a regular interval.  
  
## Syntax  
  
```  
virtual BOOL SupportsAutosaveAtInterval() const;  
```  
  
## Return Value  
 `TRUE` indicates the restart manager autosaves open documents; `FALSE` indicates the restart manager does not.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::SupportsRestartManager](../vs140/CWinApp--SupportsRestartManager.md)   
 [CWinApp::SupportsApplicationRecovery](../vs140/CWinApp--SupportsApplicationRecovery.md)   
 [CWinApp::SupportsAutosaveAtRestart](../vs140/CWinApp--SupportsAutosaveAtRestart.md)   
 [CWinApp::ReopenPreviousFilesAtRestart](../vs140/CWinApp--ReopenPreviousFilesAtRestart.md)   
 [CWinApp::RestoreAutosavedFilesAtRestart](../vs140/CWinApp--RestoreAutosavedFilesAtRestart.md)