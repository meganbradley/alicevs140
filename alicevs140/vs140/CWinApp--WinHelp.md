---
title: "CWinApp::WinHelp"
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
ms.assetid: 8cfcb0bc-6b2f-4108-be6e-ce1d38defea0
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::WinHelp
Call this member function to invoke the WinHelp application.  
  
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
 Specifies the type of help requested. For a list of possible values and how they affect the `dwData` parameter, see the [WinHelp](http://msdn.microsoft.com/library/windows/desktop/bb762267) Windows function.  
  
## Remarks  
 The framework also calls this function to invoke the WinHelp application.  
  
 The framework will automatically close the WinHelp application when your application terminates.  
  
## Example  
 [!CODE [NVC_MFCWindowing#53](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#53)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::OnContextHelp](../vs140/CWinApp--OnContextHelp.md)   
 [CWinApp::OnHelpUsing](../vs140/CWinApp--OnHelpUsing.md)   
 [CWinApp::OnHelp](../vs140/CWinApp--OnHelp.md)   
 [CWinApp::OnHelpIndex](../vs140/CWinApp--OnHelpIndex.md)   
 [WinHelp](http://msdn.microsoft.com/library/windows/desktop/bb762267)