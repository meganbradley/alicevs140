---
title: "CHtmlView::Navigate"
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
ms.assetid: 7af1aea1-14e5-4ac0-be99-5863b0640fc7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::Navigate
Call this member function to navigate to the resource identified by a URL.  
  
## Syntax  
  
```  
  
      void Navigate(  
   LPCTSTR URL,  
   DWORD dwFlags = 0,  
   LPCTSTR lpszTargetFrameName = NULL,  
   LPCTSTR lpszHeaders = NULL,  
   LPVOID lpvPostData = NULL,  
   DWORD dwPostDataLen = 0   
);  
```  
  
#### Parameters  
 *URL*  
 A caller-allocated string that contains the URL to navigate to, or the full path of the file to display.  
  
 `dwFlags`  
 The flags of a variable that specifies whether to add the resource to the history list, whether to read to or write from the cache, and whether to display the resource in a new window. The variable can be a combination of the values defined by the [BrowserNavConstants](https://msdn.microsoft.com/en-us/library/aa768360.aspx) enumeration.  
  
 `lpszTargetFrameName`  
 A pointer to a string that contains the name of the frame in which to display the resource.  
  
 `lpszHeaders`  
 A pointer to a value that specifies the HTTP headers to send to the server. These headers are added to the default Internet Explorer headers. The headers can specify such things as the action required of the server, the type of data being passed to the server, or a status code. This parameter is ignored if *URL* is not an HTTP URL.  
  
 `lpvPostData`  
 A pointer to the data to send with the HTTP POST transaction. For example, the POST transaction is used to send data gathered by an HTML form. If this parameter does not specify any post data, **Navigate** issues an HTTP GET transaction. This parameter is ignored if *URL* is not an HTTP URL.  
  
 `dwPostDataLen`  
 Data to send with the HTTP POST transaction. For example, the POST transaction is used to send data gathered by an HTML form. If this parameter does not specify any post data, **Navigate** issues an HTTP GET transaction. This parameter is ignored if *URL* is not an HTTP URL.  
  
## Remarks  
 Applies to Internet Explorer and WebBrowser.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHtmlView::Navigate2](../vs140/CHtmlView--Navigate2.md)   
 [IWebBrowser2::Navigate](https://msdn.microsoft.com/en-us/library/aa752133.aspx)