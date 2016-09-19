---
title: "CWinApp::SetHelpMode"
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
ms.assetid: 0088cc2e-8327-4bf9-b1f7-8514ba375c34
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::SetHelpMode
Sets the application's help type.  
  
## Syntax  
  
```  
  
      void SetHelpMode(  
   AFX_HELP_TYPE eHelpType  
);  
```  
  
#### Parameters  
 `eHelpType`  
 Specifies the type of help to use. See [CWinApp::m_eHelpType](../vs140/CWinApp--m_eHelpType.md) for more information.  
  
## Remarks  
 Sets the application's Help type.  
  
 To set your application's Help type to HTMLHelp, you can call [EnableHTMLHelp](../vs140/CWinApp--EnableHtmlHelp.md). Once you call `EnableHTMLHelp`, your application must use HTMLHelp as its help application. If you want to change to use WinHelp, you can call `SetHelpMode` and set `eHelpType` to **afxWinHelp**.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::GetHelpMode](../vs140/CWinApp--GetHelpMode.md)