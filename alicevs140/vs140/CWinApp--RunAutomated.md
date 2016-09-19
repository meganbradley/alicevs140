---
title: "CWinApp::RunAutomated"
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
ms.assetid: 5405b99d-d8d9-47c1-ac8f-21af9d11bd1d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::RunAutomated
Call this function to determine whether the "**/Automation**" or "**-Automation**" option is present, which indicates whether the server application was launched by a client application.  
  
## Syntax  
  
```  
  
BOOL RunAutomated( );  
```  
  
## Return Value  
 Nonzero if the option was found; otherwise 0.  
  
## Remarks  
 If present, the option is removed from the command line. For more information on OLE Automation, see the article [Automation Servers](../vs140/Automation-Servers.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::RunEmbedded](../vs140/CWinApp--RunEmbedded.md)