---
title: "CWinApp::GetApplicationRecoveryParameter"
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
ms.assetid: d3d093ca-4509-4fb3-a34f-9b7ed1f419c0
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::GetApplicationRecoveryParameter
Retrieves the input parameter for the application recovery method.  
  
## Syntax  
  
```  
virtual LPVOID GetApplicationRecoveryParameter();  
```  
  
## Return Value  
 The default input parameter for the application recovery method.  
  
## Remarks  
 The default behavior of this function returns `NULL`.  
  
 For more information, see [CWinApp::ApplicationRecoveryCallback](../vs140/CWinApp--ApplicationRecoveryCallback.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::RegisterWithRestartManager](../vs140/CWinApp--RegisterWithRestartManager.md)   
 [CWinApp::ApplicationRecoveryCallback](../vs140/CWinApp--ApplicationRecoveryCallback.md)