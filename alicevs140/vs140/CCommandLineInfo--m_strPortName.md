---
title: "CCommandLineInfo::m_strPortName"
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
ms.assetid: f2e32d03-615f-48e9-bc84-0700a283ba17
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCommandLineInfo::m_strPortName
Stores the value of the fourth non-flag parameter on the command line.  
  
## Syntax  
  
```  
  
CString m_strPortName;  
  
```  
  
## Remarks  
 This parameter is typically the name of the printer port for a Print To shell command. The default implementation of [ParseParam](../vs140/CCommandLineInfo--ParseParam.md) sets this data member only if the **/pt** flag was found on the command line.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CCommandLineInfo Class](../vs140/CCommandLineInfo-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CCommandLineInfo::m_strFileName](../vs140/CCommandLineInfo--m_strFileName.md)   
 [CCommandLineInfo::m_strPrinterName](../vs140/CCommandLineInfo--m_strPrinterName.md)   
 [CCommandLineInfo::m_strDriverName](../vs140/CCommandLineInfo--m_strDriverName.md)   
 [CWinApp::ProcessShellCommand](../vs140/CWinApp--ProcessShellCommand.md)