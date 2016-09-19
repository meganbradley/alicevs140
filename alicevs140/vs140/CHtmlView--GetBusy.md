---
title: "CHtmlView::GetBusy"
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
ms.assetid: 2a68cb6d-a625-4b37-a463-6c7d9a46de89
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::GetBusy
Call this member function to determine whether the WebBrowser control is engaged in a navigation or downloading operation.  
  
## Syntax  
  
```  
  
BOOL GetBusy( ) const;  
  
```  
  
## Return Value  
 Nonzero if the web browser is busy; otherwise zero.  
  
## Remarks  
 Applies to Internet Explorer and WebBrowser.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [IWebBrowser2::get_Busy](https://msdn.microsoft.com/en-us/library/aa752113.aspx)