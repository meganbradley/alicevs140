---
title: "CHtmlView::GetLocationURL"
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
ms.assetid: 11192373-3e1a-4bfa-8ce1-db2a7337c0bf
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::GetLocationURL
Call this member function to retrieve the URL of the resource that the WebBrowser control is currently displaying.  
  
## Syntax  
  
```  
  
CString GetLocationURL( ) const;  
  
```  
  
## Return Value  
 A [CString](../vs140/CStringT-Class.md) object containing the URL of the resource currently displayed in the WebBrowser.  
  
## Remarks  
 If the resource is a folder or file on the network or local computer, the name is the UNC or full path of the folder or file.  
  
 Applies to Internet Explorer and WebBrowser.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHtmlView::GetLocationName](../vs140/CHtmlView--GetLocationName.md)   
 [IWebBrowser2::get_LocationURL](https://msdn.microsoft.com/en-us/library/aa752130.aspx)