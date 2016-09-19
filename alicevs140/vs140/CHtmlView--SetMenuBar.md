---
title: "CHtmlView::SetMenuBar"
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
ms.assetid: 489d19ba-3877-4bab-8f81-d5647eb2bd89
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::SetMenuBar
Call this member function to show or hide the Internet Explorer menu bar.  
  
## Syntax  
  
```  
  
      void SetMenuBar(  
   BOOL bNewValue   
);  
```  
  
#### Parameters  
 `bNewValue`  
 Nonzero to show menu bar; otherwise zero.  
  
## Remarks  
 Applies to Internet Explorer. If you use this call with a WebBrowser control, it will return no error, but it will ignore this call.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHtmlView::GetMenuBar](../vs140/CHtmlView--GetMenuBar.md)   
 [IWebBrowser2::put_MenuBar](https://msdn.microsoft.com/en-us/library/aa752131.aspx)