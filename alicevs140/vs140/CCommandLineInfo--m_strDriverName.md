---
title: "CCommandLineInfo::m_strDriverName"
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
ms.assetid: e5b6bd3f-85b1-45ec-9426-95f35446ac62
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCommandLineInfo::m_strDriverName
Stores the value of the third non-flag parameter on the command line.  
  
## Syntax  
  
```  
  
CString m_strDriverName;  
  
```  
  
## Remarks  
 This parameter is typically the name of the printer driver for a Print To shell command. The default implementation of [ParseParam](../vs140/CCommandLineInfo--ParseParam.md) sets this data member only if the **/pt** flag was found on the command line.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CCommandLineInfo Class](../vs140/CCommandLineInfo-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CCommandLineInfo::m_strFileName](../vs140/CCommandLineInfo--m_strFileName.md)   
 [CCommandLineInfo::m_strPrinterName](../vs140/CCommandLineInfo--m_strPrinterName.md)   
 [CCommandLineInfo::m_strPortName](../vs140/CCommandLineInfo--m_strPortName.md)   
 [CWinApp::ProcessShellCommand](../vs140/CWinApp--ProcessShellCommand.md)