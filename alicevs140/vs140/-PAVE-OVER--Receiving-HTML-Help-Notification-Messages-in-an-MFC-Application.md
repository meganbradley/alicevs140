---
title: "&lt;PAVE OVER&gt; Receiving HTML Help Notification Messages in an MFC Application"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4b917eac-03c9-4c4d-a67e-a5eaa26c2a26
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;PAVE OVER&gt; Receiving HTML Help Notification Messages in an MFC Application
To receive notification messages from HTML Help within an MFC program, you must:  
  
1.  Define a symbol in your Visual C++ project. This example uses a symbol called ID_HHNOTIFICATION.  
  
    -   To define a symbol, right-click the high-level folder in **ResourceView** and select **Resource Symbols**.  
  
    -   In the **Resource Symbols** dialog box, click `New` and define the new symbol.  
  
2.  In your Visual C++ project, initialize the **HH_WINTYPE** structure and call the `HTMLHelp` function to set this structure using the **HH_SET_WIN_TYPE** command. Use **ID_HHNOTIFICATION** for the *idNotify* field in the structure.  
  
3.  Override the `OnNotify` function in the derivative of the `CWnd` class that you want to receive the message (the `CWnd` class associated with `HWND` specified in the **hwndCaller** field of the **WW_WINTYPE** structure). The following example shows how an `OnNotify` function is used to call an **OnNavComplete(HHN_NOTIFY\*, LRESULT)** handler whenever HTML Help navigates to a topic:  
  
     [!CODE [NVC_MFCHtmlHelp#5](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCHtmlHelp#5)]  
  
## See Also  
 [HTML Help: Context-Sensitive Help for Your Programs](../vs140/HTML-Help--Context-Sensitive-Help-for-Your-Programs.md)