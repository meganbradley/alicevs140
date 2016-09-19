---
title: "CHtmlView::SetTheaterMode"
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
ms.assetid: 478b1ce3-7a14-445d-96bd-d0ad438fd9b7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::SetTheaterMode
Call this member function to set a value indicating whether the WebBrowser control is in theater mode.  
  
## Syntax  
  
```  
  
      void SetTheaterMode(  
   BOOL bNewValue   
);  
```  
  
#### Parameters  
 `bNewValue`  
 Nonzero to set the WebBrowser control to theater mode; otherwise zero. The default value is zero.  
  
## Remarks  
 When the web browser is in theater mode, the browser main window fills the entire screen, a toolbar with a minimal set of navigational tools appears, and the status bar appears in the upper right-hand corner of the screen.  
  
 Applies to Internet Explorer and WebBrowser.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHtmlView::GetTheaterMode](../vs140/CHtmlView--GetTheaterMode.md)   
 [CHtmlView::GetFullScreen](../vs140/CHtmlView--GetFullScreen.md)   
 [CHtmlView::SetFullScreen](../vs140/CHtmlView--SetFullScreen.md)