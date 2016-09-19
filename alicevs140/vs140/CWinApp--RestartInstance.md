---
title: "CWinApp::RestartInstance"
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
ms.assetid: 3121aa4f-1cc5-452d-b7b4-9f90580e9ee8
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::RestartInstance
Handles an application restart initiated by the restart manager.  
  
## Syntax  
  
```  
virtual BOOL CWinApp::RestartInstance();  
```  
  
## Return Value  
 `TRUE` if the data recovery handler opens previously open documents; `FALSE` if the data recovery handler has an error or if there are no previously open documents.  
  
## Remarks  
 When the restart manager restarts an application, the framework calls this method. This method retrieves the data recovery handler and restores the autosaved files. This method calls [CDataRecoveryHandler::RestoreAutosavedDocuments](../vs140/CDataRecoveryHandler--RestoreAutosavedDocuments.md) to determine whether the user wants to restore the autosaved files.  
  
 This method returns `FALSE` if the [CDataRecoveryHandler](../vs140/CDataRecoveryHandler-Class.md) determines that there were no open documents. If there were no open documents, the application starts ordinarily.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDataRecoveryHandler Class](../vs140/CDataRecoveryHandler-Class.md)