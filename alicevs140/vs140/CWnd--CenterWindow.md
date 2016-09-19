---
title: "CWnd::CenterWindow"
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
ms.assetid: 27d0d7d1-374a-4e73-8639-004291b634b9
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::CenterWindow
Centers a window relative to its parent.  
  
## Syntax  
  
```  
  
      void CenterWindow(  
   CWnd* pAlternateOwner = NULL   
);  
```  
  
#### Parameters  
 `pAlternateOwner`  
 Pointer to an alternate window relative to which it will be centered (other than the parent window).  
  
## Remarks  
 Usually called from [CDialog::OnInitDialog](../vs140/CDialog--OnInitDialog.md) to center dialog boxes relative to the main window of the application. By default, the function centers child windows relative to their parent window, and pop-up windows relative to their owner. If the pop-up window is not owned, it is centered relative to the screen. To center a window relative to a specific window which is not the owner or parent, the `pAlternateOwner` parameter may be set to a valid window. To force centering relative to the screen, pass the value returned by [CWnd::GetDesktopWindow](../vs140/CWnd--GetDesktopWindow.md) as `pAlternateOwner`.  
  
## Example  
 [!CODE [NVC_MFCWindowing#74](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#74)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::GetDesktopWindow](../vs140/CWnd--GetDesktopWindow.md)   
 [CDialog::OnInitDialog](../vs140/CDialog--OnInitDialog.md)