---
title: "CHtmlView::SetRegisterAsBrowser"
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
ms.assetid: a3f393df-2a38-47a2-ab76-50c97b50fe1c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::SetRegisterAsBrowser
Call this member function to set a value indicating whether the WebBrowser control is registered as a top-level browser for target name resolution.  
  
## Syntax  
  
```  
  
      void SetRegisterAsBrowser(  
   BOOL bNewValue   
);  
```  
  
#### Parameters  
 `bNewValue`  
 Determines whether Internet Explorer is registered as a top-level browser. If nonzero, the web browser is registered as a top-level browser; if zero, it is not a top-level browser. The default value is zero.  
  
## Remarks  
 A top-level browser is the browser set in the registry as the default browser.  
  
 Applies to Internet Explorer and WebBrowser.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHtmlView::GetRegisterAsBrowser](../vs140/CHtmlView--GetRegisterAsBrowser.md)   
 [IWebBrowser2::put_RegisterAsBrowser](https://msdn.microsoft.com/en-us/library/aa768264.aspx)