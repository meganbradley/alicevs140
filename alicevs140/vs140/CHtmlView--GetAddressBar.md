---
title: "CHtmlView::GetAddressBar"
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
ms.assetid: 2503498d-fd90-4773-a0b9-90f78b158629
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::GetAddressBar
Call this member function to retrieve Internet Explorer's address bar.  
  
## Syntax  
  
```  
  
BOOL GetAddressBar( ) const;  
  
```  
  
## Return Value  
 Nonzero if the address bar is visible; otherwise zero.  
  
## Remarks  
 Applies to Internet Explorer. If you use this call with a WebBrowser control, it will return no error, but it will ignore this call.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHtmlView::SetAddressBar](../vs140/CHtmlView--SetAddressBar.md)   
 [IWebBrowser2::get_AddressBar](https://msdn.microsoft.com/en-us/library/aa752110.aspx)