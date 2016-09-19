---
title: "CWinApp::m_hInstance"
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
ms.assetid: 7344f586-6956-4c36-9131-af8cced9eb67
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::m_hInstance
Corresponds to the `hInstance` parameter passed by Windows to `WinMain`.  
  
## Syntax  
  
```  
  
HINSTANCE m_hInstance;  
  
```  
  
## Remarks  
 The `m_hInstance` data member is a handle to the current instance of the application running under Windows. This is returned by the global function [AfxGetInstanceHandle](../vs140/AfxGetInstanceHandle.md). `m_hInstance` is a public variable of type `HINSTANCE`.  
  
## Example  
 [!CODE [NVC_MFCWindowing#55](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#55)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)