---
title: "CWinApp::m_nCmdShow"
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
ms.assetid: ba1c0117-3446-4613-ac56-ff1433515d19
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::m_nCmdShow
Corresponds to the `nCmdShow` parameter passed by Windows to `WinMain`.  
  
## Syntax  
  
```  
  
int m_nCmdShow;  
  
```  
  
## Remarks  
 You should pass `m_nCmdShow` as an argument when you call [CWnd::ShowWindow](../vs140/CWnd--ShowWindow.md) for your application's main window. `m_nCmdShow` is a public variable of type `int`.  
  
## Example  
 [!CODE [NVC_MFCWindowing#56](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#56)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)