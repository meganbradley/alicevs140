---
title: "CWinApp::ApplicationRecoveryCallback"
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
ms.assetid: 477ec2db-40ea-4e42-9710-de1596cdb1fe
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::ApplicationRecoveryCallback
Called by the framework when the application unexpectedly exits.  
  
## Syntax  
  
```  
virtual DWORD ApplicationRecoveryCallback(  
   LPVOID lpvParam  
);  
```  
  
#### Parameters  
 [in] `lpvParam`  
 Reserved for future use.  
  
## Return Value  
 0 if this method is successful; nonzero if an error occurs.  
  
## Remarks  
 If your application supports the restart manager, the framework calls this function when your application unexpectedly exits.  
  
 The default implementation of `ApplicationRecoveryCallback` uses the `CDataRecoveryHandler` to save the list of currently open documents to the registry. This method does not autosave any files.  
  
 To customize the behavior, override this function in a derived [CWinApp Class](../vs140/CWinApp-Class.md) or pass your own application recovery method as a parameter to [CWinApp::RegisterWithRestartManager](../vs140/CWinApp--RegisterWithRestartManager.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::RegisterWithRestartManager](../vs140/CWinApp--RegisterWithRestartManager.md)   
 [CDataRecoveryHandler Class](../vs140/CDataRecoveryHandler-Class.md)