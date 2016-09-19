---
title: "CWinApp::OnHelpUsing"
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
ms.assetid: 1ea0cbb1-23a9-4893-81b6-e7a7f514c241
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::OnHelpUsing
Handles the **ID_HELP_USING** command.  
  
## Syntax  
  
```  
  
afx_msg void OnHelpUsing( );  
```  
  
## Remarks  
 You must add an `ON_COMMAND( ID_HELP_USING, OnHelpUsing )` statement to your `CWinApp` class message map to enable this member function. The framework calls this message-handler function when the user of your application selects the Help Using command to invoke the `WinHelp` application with the standard **HELP_HELPONHELP** topic.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::OnHelp](../vs140/CWinApp--OnHelp.md)   
 [CWinApp::OnHelpIndex](../vs140/CWinApp--OnHelpIndex.md)   
 [CWinApp::WinHelp](../vs140/CWinApp--WinHelp.md)