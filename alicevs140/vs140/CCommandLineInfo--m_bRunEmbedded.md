---
title: "CCommandLineInfo::m_bRunEmbedded"
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
ms.assetid: 2b420f1c-95a5-4b62-9d6f-f994486350e7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCommandLineInfo::m_bRunEmbedded
Indicates that the **/Embedding** flag was found on the command line.  
  
## Syntax  
  
```  
  
BOOL m_bRunEmbedded;  
  
```  
  
## Remarks  
 If **TRUE**, this means start up for editing an embedded OLE item.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CCommandLineInfo Class](../vs140/CCommandLineInfo-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CCommandLineInfo::m_bShowSplash](../vs140/CCommandLineInfo--m_bShowSplash.md)   
 [CWinApp::ProcessShellCommand](../vs140/CWinApp--ProcessShellCommand.md)