---
title: "CCommandLineInfo::m_bShowSplash"
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
ms.assetid: 05aae7de-240b-4c11-9b5f-90dd82352e77
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCommandLineInfo::m_bShowSplash
Indicates that the splash screen should be displayed.  
  
## Syntax  
  
```  
  
BOOL m_bShowSplash;  
  
```  
  
## Remarks  
 If **TRUE**, this means the splash screen for this application should be displayed during startup. The default implementation of [ParseParam](../vs140/CCommandLineInfo--ParseParam.md) sets this data member to **TRUE** if [m_nShellCommand](../vs140/CCommandLineInfo--m_nShellCommand.md) is equal to **CCommandLineInfo::FileNew**.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CCommandLineInfo Class](../vs140/CCommandLineInfo-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CCommandLineInfo::m_bRunAutomated](../vs140/CCommandLineInfo--m_bRunAutomated.md)   
 [CCommandLineInfo::m_bRunEmbedded](../vs140/CCommandLineInfo--m_bRunEmbedded.md)   
 [CCommandLineInfo::m_nShellCommand](../vs140/CCommandLineInfo--m_nShellCommand.md)   
 [CCommandLineInfo::ParseParam](../vs140/CCommandLineInfo--ParseParam.md)   
 [CWinApp::ProcessShellCommand](../vs140/CWinApp--ProcessShellCommand.md)