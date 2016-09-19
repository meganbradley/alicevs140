---
title: "CWinApp::m_eHelpType"
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
ms.assetid: 5a481f8f-e6b1-4890-a4f8-7b81cac0b154
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::m_eHelpType
The type of this data member is the enumerated type **AFX_HELP_TYPE**, which is defined within the `CWinApp` class.  
  
## Syntax  
  
```  
  
AFX_HELP_TYPE m_eHelpType;  
  
```  
  
## Remarks  
 The **AFX_HELP_TYPE** enumeration is defined as follows:  
  
 `enum AFX_HELP_TYPE`  
  
 `{`  
  
 `afxWinHelp = 0,`  
  
 `afxHTMLHelp = 1`  
  
 `};`  
  
-   To set the application's help to HTML Help, call [SetHelpMode](../vs140/CWinApp--SetHelpMode.md) and specify **afxHTMLHelp**.  
  
-   To set the application's help to WinHelp, call `SetHelpMode` and specify **afxWinHelp**.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::GetHelpMode](../vs140/CWinApp--GetHelpMode.md)   
 [CWinApp::EnableHtmlHelp](../vs140/CWinApp--EnableHtmlHelp.md)