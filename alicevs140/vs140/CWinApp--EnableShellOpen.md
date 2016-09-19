---
title: "CWinApp::EnableShellOpen"
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
ms.assetid: d73c8842-493d-4948-b2ea-4c68308b1be9
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::EnableShellOpen
Call this function, typically from your `InitInstance` override, to enable your application's users to open data files when they double-click the files from within the Windows File Manager.  
  
## Syntax  
  
```  
  
void EnableShellOpen( );  
```  
  
## Remarks  
 Call the `RegisterShellFileTypes` member function in conjunction with this function, or provide a .REG file with your application for manual registration of document types.  
  
## Example  
 [!CODE [NVC_MFCWindowing#38](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#38)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::OnDDECommand](../vs140/CWinApp--OnDDECommand.md)   
 [CWinApp::RegisterShellFileTypes](../vs140/CWinApp--RegisterShellFileTypes.md)