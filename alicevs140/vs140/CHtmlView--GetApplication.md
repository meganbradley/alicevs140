---
title: "CHtmlView::GetApplication"
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
ms.assetid: f07012b4-3a4c-4052-a65e-72cf0edc301b
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::GetApplication
Call this member function to retrieve the automation object supported by the application that contains the WebBrowser control.  
  
## Syntax  
  
```  
  
LPDISPATCH GetApplication( ) const;  
  
```  
  
## Return Value  
 A pointer to the `IDispatch` interface of the active document object. For more information, see [Implementing the IDispatch Interface](assetId:///0e171f7f-0022-4e9b-ac8e-98192828e945).  
  
## Remarks  
 Applies to Internet Explorer and WebBrowser.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [IWebBrowser2::get_Application](https://msdn.microsoft.com/en-us/library/aa752112.aspx)