---
title: "CWinApp::Register"
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
ms.assetid: 624d6071-4fef-44cf-b53a-bf8cdbfccf00
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::Register
Performs any registration tasks not handled by `RegisterShellFileTypes`.  
  
## Syntax  
  
```  
  
virtual BOOL Register( );  
  
```  
  
## Return Value  
 Nonzero on success; otherwise 0.  
  
## Remarks  
 The default implementation simply returns TRUE. Override this function to provide any customized registration steps.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::RegisterShellFileTypes](../vs140/CWinApp--RegisterShellFileTypes.md)