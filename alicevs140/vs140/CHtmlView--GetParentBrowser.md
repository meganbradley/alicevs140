---
title: "CHtmlView::GetParentBrowser"
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
ms.assetid: 2e39e19a-92b4-4cc5-af04-5e9c4bee2599
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::GetParentBrowser
Call this member function to retrieve a pointer to the parent object of the WebBrowser control.  
  
## Syntax  
  
```  
  
LPDISPATCH GetParentBrowser( ) const;  
  
```  
  
## Return Value  
 A pointer to the `IDispatch` interface of the object that is the parent of the WebBrowser control.  
  
## Remarks  
 Applies to Internet Explorer and WebBrowser.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [IWebBrowser2::get_Parent](https://msdn.microsoft.com/en-us/library/aa752136.aspx)