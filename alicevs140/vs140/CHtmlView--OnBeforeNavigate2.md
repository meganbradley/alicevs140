---
title: "CHtmlView::OnBeforeNavigate2"
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
ms.assetid: e73c4f24-2038-495c-bb16-1077b400e438
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::OnBeforeNavigate2
This member function is called by the framework to cause an event to fire before a navigation occurs in the web browser.  
  
## Syntax  
  
```  
  
      virtual void OnBeforeNavigate2(  
   LPCTSTR lpszURL,  
   DWORD nFlags,  
   LPCTSTR lpszTargetFrameName,  
   CByteArray& baPostedData,  
   LPCTSTR lpszHeaders,  
   BOOL* pbCancel   
);  
```  
  
#### Parameters  
 `lpszURL`  
 Pointer to a string containing the URL to navigate to.  
  
 `nFlags`  
 Reserved for future use.  
  
 `lpszTargetFrameName`  
 A string that contains the name of the frame in which to display the resource, or **NULL** if no named frame is targeted for the resource.  
  
 `baPostedData`  
 A reference to a `CByteArray` object containing the data to send to the server if the HTTP POST transaction is being used.  
  
 `lpszHeaders`  
 A pointer to a string containing additional HTTP headers to send to the server (HTTP URLs only). The headers can specify such things as the action required of the server, the type of data being passed to the server, or a status code.  
  
 `pbCancel`  
 A pointer to a cancel flag. An application can set this parameter to nonzero to cancel the navigation operation, or to zero to allow it to proceed.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHtmlView::Navigate](../vs140/CHtmlView--Navigate.md)   
 [CHtmlView::Navigate2](../vs140/CHtmlView--Navigate2.md)   
 [DWebBrowserEvents2::BeforeNavigate2](https://msdn.microsoft.com/en-us/library/aa768280.aspx)