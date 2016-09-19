---
title: "CHtmlView::SetOffline"
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
ms.assetid: 6325e285-7ff4-475a-b16a-f4e90967bbde
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::SetOffline
Call this member function to set a value indicating whether the WebBrowser control is currently operating in offline mode.  
  
## Syntax  
  
```  
  
      void SetOffline(  
   BOOL bNewValue   
);  
```  
  
#### Parameters  
 `bNewValue`  
 Nonzero to read from the local cache; otherwise zero.  
  
## Remarks  
 In offline mode, the browser reads HTML pages from the local cache rather than from the source document.  
  
 Applies to Internet Explorer and WebBrowser.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHtmlView::GetOffline](../vs140/CHtmlView--GetOffline.md)   
 [IWebBrowser2::put_Offline](https://msdn.microsoft.com/en-us/library/aa752135.aspx)