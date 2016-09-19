---
title: "CHtmlView::GetTheaterMode"
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
ms.assetid: a43b83e8-a273-495e-abfc-49e2e898bf6e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::GetTheaterMode
Call this member function to determine whether the web browser is in theater mode.  
  
## Syntax  
  
```  
  
BOOL GetTheaterMode( ) const;  
  
```  
  
## Return Value  
 Nonzero if the web browser is in theater mode; otherwise zero.  
  
## Remarks  
 When the web browser is in theater mode, the browser main window fills the entire screen, a toolbar with a minimal set of navigational tools appears, and the status bar appears in the upper right-hand corner of the screen.  
  
 Applies to Internet Explorer and WebBrowser.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHtmlView::SetTheaterMode](../vs140/CHtmlView--SetTheaterMode.md)   
 [CHtmlView::SetFullScreen](../vs140/CHtmlView--SetFullScreen.md)   
 [IWebBrowser2::get_TheaterMode](https://msdn.microsoft.com/en-us/library/aa768273.aspx)