---
title: "CHtmlView::GetFullScreen"
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
ms.assetid: 92c53ce9-f1bb-4624-bbe3-458379ed0728
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::GetFullScreen
Call this member function to determine whether the WebBrowser control is operating in full-screen mode or in normal window mode.  
  
## Syntax  
  
```  
  
BOOL GetFullScreen( ) const;  
  
```  
  
## Return Value  
 Nonzero if the WebBrowser is operating in full-screen mode; otherwise zero.  
  
## Remarks  
 In full-screen mode, the Internet Explorer main window is maximized and the status bar, toolbar, menu bar, and title bar are hidden.  
  
 Applies to Internet Explorer and WebBrowser.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHtmlView::SetFullScreen](../vs140/CHtmlView--SetFullScreen.md)   
 [IWebBrowser2::get_FullScreen](https://msdn.microsoft.com/en-us/library/aa752119.aspx)