---
title: "CHtmlView::GetHtmlDocument"
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
ms.assetid: 63e0d2aa-de5b-43c0-8706-b53f3ee41c85
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::GetHtmlDocument
Call this member function to retrieve the HTML document for the active document.  
  
## Syntax  
  
```  
  
LPDISPATCH GetHtmlDocument( ) const;  
  
```  
  
## Return Value  
 A pointer to the `IDispatch` interface of the active document object.  
  
## Remarks  
 Applies to Internet Explorer and WebBrowser.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [IWebBrowser2::get_Document](https://msdn.microsoft.com/en-us/library/aa752116.aspx)