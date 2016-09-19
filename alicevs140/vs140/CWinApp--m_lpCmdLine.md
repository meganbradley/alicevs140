---
title: "CWinApp::m_lpCmdLine"
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
ms.assetid: c29fd6e9-47cd-4fec-91c8-62c91a794c98
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::m_lpCmdLine
Corresponds to the `lpCmdLine` parameter passed by Windows to `WinMain`.  
  
## Syntax  
  
```  
  
LPTSTR m_lpCmdLine;  
  
```  
  
## Remarks  
 Points to a null-terminated string that specifies the command line for the application. Use `m_lpCmdLine` to access any command-line arguments the user entered when the application was started. `m_lpCmdLine` is a public variable of type `LPTSTR`.  
  
## Example  
 [!CODE [NVC_MFCWindowing#52](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#52)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)