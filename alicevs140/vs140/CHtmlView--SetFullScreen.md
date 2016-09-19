---
title: "CHtmlView::SetFullScreen"
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
ms.assetid: 47d39120-f5cb-4710-bf91-3d534c07403b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::SetFullScreen
Call this member function to set Internet Explorer to either full-screen or normal window mode.  
  
## Syntax  
  
```  
  
      void SetFullScreen(  
   BOOL bNewValue   
);  
```  
  
#### Parameters  
 `bNewValue`  
 Nonzero for full-screen mode; otherwise zero.  
  
## Remarks  
 In full-screen mode, the Internet Explorer main window is maximized and the status bar, toolbar, menu bar, and title bar are hidden.  
  
 Applies to Internet Explorer. If you use this call with a WebBrowser control, it will return no error, but it will ignore this call.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHtmlView::GetFullScreen](../vs140/CHtmlView--GetFullScreen.md)   
 [CHtmlView::SetTheaterMode](../vs140/CHtmlView--SetTheaterMode.md)   
 [IWebBrowser2::put_FullScreen](https://msdn.microsoft.com/en-us/library/aa752119.aspx)