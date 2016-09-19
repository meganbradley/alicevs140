---
title: "CHtmlView::SetStatusBar"
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
ms.assetid: e489f96e-1a31-44bc-a97d-7c3a12743bed
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::SetStatusBar
Call this member function to display the status bar.  
  
## Syntax  
  
```  
  
      void SetStatusBar(  
   BOOL bNewValue   
);  
```  
  
#### Parameters  
 `bNewValue`  
 Nonzero if the status bar is visible; otherwise zero.  
  
## Remarks  
 Applies to Internet Explorer. If you use this call with a WebBrowser control, it will return no error, but it will ignore this call.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHtmlView::GetStatusBar](../vs140/CHtmlView--GetStatusBar.md)   
 [IWebBrowser2::put_StatusBar](https://msdn.microsoft.com/en-us/library/aa768270.aspx)