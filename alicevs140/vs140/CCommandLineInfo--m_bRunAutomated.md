---
title: "CCommandLineInfo::m_bRunAutomated"
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
ms.assetid: a991488c-9f27-44be-9a9e-0ddbbcf388df
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCommandLineInfo::m_bRunAutomated
Indicates that the **/Automation** flag was found on the command line.  
  
## Syntax  
  
```  
  
BOOL m_bRunAutomated;  
  
```  
  
## Remarks  
 If **TRUE**, this means start up as an OLE automation server.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CCommandLineInfo Class](../vs140/CCommandLineInfo-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CCommandLineInfo::ParseParam](../vs140/CCommandLineInfo--ParseParam.md)   
 [CWinApp::ProcessShellCommand](../vs140/CWinApp--ProcessShellCommand.md)