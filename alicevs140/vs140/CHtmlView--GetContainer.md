---
title: "CHtmlView::GetContainer"
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
ms.assetid: 162f7c12-14f7-4e83-a27b-20d6ba5deb00
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::GetContainer
Call this member function to retrieve an object that evaluates to the container of the web browser.  
  
## Syntax  
  
```  
  
LPDISPATCH GetContainer( ) const;  
  
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
 [CHtmlView::GetTopLevelContainer](../vs140/CHtmlView--GetTopLevelContainer.md)   
 [IWebBrowser2::get_Container](https://msdn.microsoft.com/en-us/library/aa752115.aspx)