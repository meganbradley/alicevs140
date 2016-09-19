---
title: "CHtmlView::GetStatusBar"
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
ms.assetid: ce74253b-840c-477c-9d05-32d0a4569dd7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::GetStatusBar
Call this member function to determine whether the WebBrowser control displays a status bar.  
  
## Syntax  
  
```  
  
BOOL GetStatusBar( ) const;  
  
```  
  
## Return Value  
 Nonzero if the status bar can be displayed; otherwise zero.  
  
## Remarks  
 Applies to Internet Explorer. If you use this call with a WebBrowser control, it will return no error, but it will ignore this call.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHtmlView::SetStatusBar](../vs140/CHtmlView--SetStatusBar.md)   
 [IWebBrowser2::get_StatusBar](https://msdn.microsoft.com/en-us/library/aa768270.aspx)