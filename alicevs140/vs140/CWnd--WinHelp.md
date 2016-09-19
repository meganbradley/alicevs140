---
title: "CWnd::WinHelp"
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
ms.assetid: d09916e0-9fc0-4986-9a74-35e6c4a37fbc
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::WinHelp
Called to initiate the WinHelp application.  
  
## Syntax  
  
```  
  
      virtual void WinHelp(  
   DWORD_PTR dwData,  
   UINT nCmd = HELP_CONTEXT   
);  
```  
  
#### Parameters  
 `dwData`  
 Specifies additional data. The value used depends on the value of the `nCmd` parameter.  
  
 `nCmd`  
 Specifies the type of help requested. For a list of possible values and how they affect the `dwData` parameter, see the [WinHelp](http://msdn.microsoft.com/library/windows/desktop/bb762267) Windows function in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Remarks  
 See [CWinApp::WinHelp](../vs140/CWinApp--WinHelp.md) for more information.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::HtmlHelp](../vs140/CWnd--HtmlHelp.md)   
 [CWnd::OnHelpUsing](../vs140/CWnd--OnHelpUsing.md)   
 [CWnd::OnHelpIndex](../vs140/CWnd--OnHelpIndex.md)