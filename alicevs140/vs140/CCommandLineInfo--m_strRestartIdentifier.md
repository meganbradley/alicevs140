---
title: "CCommandLineInfo::m_strRestartIdentifier"
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
ms.assetid: f5520ff2-5ea5-408f-8dc1-8d3f4be78b84
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCommandLineInfo::m_strRestartIdentifier
The unique restart identifier on the command line.  
  
## Syntax  
  
```  
CString m_strRestartIdentifier;  
```  
  
## Remarks  
 The restart identifier is unique for each instance of the application.  
  
 If the restart manager exits the application and is configured to restart it, the restart manager executes the application from the command line with the restart identifier as an optional parameter. When the restart manager uses the restart identifier, the application can reopen the previously open documents and recover autosaved files.  
  
## Requirements  
 `Header:` afxwin.h  
  
## See Also  
 [CCommandLineInfo Class](../vs140/CCommandLineInfo-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDataRecoveryHandler Class](../vs140/CDataRecoveryHandler-Class.md)   
 [CDataRecoveryHandler::GetRestartIdentifier](../vs140/CDataRecoveryHandler--GetRestartIdentifier.md)   
 [CDataRecoveryHandler::SetRestartIdentifier](../vs140/CDataRecoveryHandler--SetRestartIdentifier.md)