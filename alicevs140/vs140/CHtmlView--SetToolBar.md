---
title: "CHtmlView::SetToolBar"
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
ms.assetid: 666cab0b-47c2-4203-8cf2-7448bcf1b7bb
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::SetToolBar
Call this member function to show or hide the Internet Explorer toolbar.  
  
## Syntax  
  
```  
  
      void SetToolBar(  
   int nNewValue   
);  
```  
  
#### Parameters  
 `nNewValue`  
 Indicates whether to display the toolbar. Nonzero if the toolbar is to be displayed; otherwise zero.  
  
## Remarks  
 Applies to Internet Explorer. If you use this call with a WebBrowser control, it will return no error, but it will ignore this call.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHtmlView::GetToolBar](../vs140/CHtmlView--GetToolBar.md)   
 [IWebBrowser2::put_ToolBar](https://msdn.microsoft.com/en-us/library/aa768274.aspx)