---
title: "CHtmlView::GetRegisterAsBrowser"
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
ms.assetid: 03a0dba6-f4e2-4eb5-bdc8-436d13e0a2b7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::GetRegisterAsBrowser
Call this member function to determine whether the WebBrowser object is registered as a top-level browser for target name resolution.  
  
## Syntax  
  
```  
  
BOOL GetRegisterAsBrowser( ) const;  
  
```  
  
## Return Value  
 Nonzero if the browser is registered as a top-level browser; otherwise zero.  
  
## Remarks  
 Applies to Internet Explorer and WebBrowser.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHtmlView::SetRegisterAsBrowser](../vs140/CHtmlView--SetRegisterAsBrowser.md)   
 [IWebBrowser2::get_RegisterAsBrowser](https://msdn.microsoft.com/en-us/library/aa768264.aspx)