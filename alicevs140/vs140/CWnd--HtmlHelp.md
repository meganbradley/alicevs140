---
title: "CWnd::HtmlHelp"
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
ms.assetid: 79f214fa-116b-43b8-adb4-a0fdfcb38ac5
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::HtmlHelp
Call this member function to invoke the HTMLHelp application.  
  
## Syntax  
  
```  
  
      virtual void HtmlHelp(  
   DWORD_PTR dwData,  
   UINT nCmd = 0x000F   
);  
```  
  
#### Parameters  
 `dwData`  
 Specifies additional data. The value used depends on the value of the `nCmd` parameter.  
  
 `nCmd`  
 Specifies the type of help requested. For a list of possible values and how they affect the `dwData` parameter, see the `uCommand` parameter described in the [HTMLHelp API Reference](vsconOvhtmlhelpapioverview) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Remarks  
 See [CWinApp::HtmlHelp](../vs140/CWinApp--HtmlHelp.md) for more information.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::WinHelp](../vs140/CWnd--WinHelp.md)   
 [<PAVE OVER\> Displaying F1 Help for a Dialog Box or Menu Option](../vs140/-PAVE-OVER--Displaying-F1-Help-for-a-Dialog-Box-or-Menu-Option.md)