---
title: "CWnd::OnTCard"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: f627b838-4695-499a-bd97-7361e510946f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnTCard
The framework calls this member function when the user clicks an authorable button.  
  
## Syntax  
  
```  
  
      afx_msg void OnTCard(  
   UINT idAction,  
   DWORD dwActionData   
);  
```  
  
#### Parameters  
 `idAction`  
 Indicates the action the user has taken. This parameter can be one of these values:  
  
-   **IDABORT** The user clicked an authorable Abort button.  
  
-   **IDCANCEL** The user clicked an authorable Cancel button.  
  
-   **IDCLOSE** The user closed the training card.  
  
-   **IDHELP** The user clicked an authorable Windows Help button.  
  
-   **IDIGNORE** The user clicked an authorable Ignore button.  
  
-   **IDOK** The user clicked an authorable OK button.  
  
-   **IDNO** The user clicked an authorable No button.  
  
-   **IDRETRY** The user clicked an authorable Retry button.  
  
-   **HELP_TCARD_DATA** The user clicked an authorable button. The `dwActionData` parameter contains a long integer specified by the help author.  
  
-   **HELP_TCARD_NEXT** The user clicked an authorable Next button.  
  
-   **HELP_TCARD_OTHER_CALLER** Another application has requested training cards.  
  
-   **IDYES** The user clicked an authorable Yes button.  
  
 `dwActionData`  
 If `idAction` specifies **HELP_TCARD_DATA**, this parameter is a long integer specified by the help author. Otherwise, this parameter is zero.  
  
## Remarks  
 This function is called only when an application has initiated a training card with Windows Help. An application initiates a training card by specifying the **HELP_TCARD** command in a call to the [WinHelp](../vs140/CWinApp--WinHelp.md) function.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [WinHelp](http://msdn.microsoft.com/library/windows/desktop/bb762267)   
 [CWinApp::WinHelp](../vs140/CWinApp--WinHelp.md)