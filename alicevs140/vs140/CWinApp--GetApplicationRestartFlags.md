---
title: "CWinApp::GetApplicationRestartFlags"
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
ms.assetid: 83661f1e-d295-44a8-8ae1-b5d45d1e62cc
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::GetApplicationRestartFlags
Returns the flags for the restart manager.  
  
## Syntax  
  
```  
virtual DWORD GetApplicationRestartFlags();  
```  
  
## Return Value  
 The flags for the restart manager. The default implementation returns 0.  
  
## Remarks  
 The flags for the restart manager have no effect with the default implementation. They are provided for future use.  
  
 You set the flags when you register the application with the restart manager by using [CWinApp::RegisterWithRestartManager](../vs140/CWinApp--RegisterWithRestartManager.md).  
  
 The possible values for the restart manager flags are as follows:  
  
-   `RESTART_NO_CRASH`  
  
-   `RESTART_NO_HANG`  
  
-   `RESTART_NO_PATCH`  
  
-   `RESTART_NO_REBOOT`  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::RegisterWithRestartManager](../vs140/CWinApp--RegisterWithRestartManager.md)