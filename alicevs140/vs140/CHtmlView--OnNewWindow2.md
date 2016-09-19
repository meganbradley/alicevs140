---
title: "CHtmlView::OnNewWindow2"
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
ms.assetid: 22216320-25fd-42f4-bb61-61f87a787796
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::OnNewWindow2
This member function is called by the framework when a new window is to be created for displaying a resource.  
  
## Syntax  
  
```  
  
      virtual void OnNewWindow2(  
   LPDISPATCH* ppDisp,  
   BOOL* Cancel   
);  
```  
  
#### Parameters  
 `ppDisp`  
 A pointer to an interface pointer that, optionally, receives the `IDispatch` interface pointer of a new WebBrowser or Internet Explorer object.  
  
 `Cancel`  
 A pointer to a cancel flag. An application can set this parameter to nonzero to cancel the navigation operation, or to zero to allow it to proceed.  
  
## Remarks  
 This event precedes the creation of a new window from within the WebBrowser.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [DWebBrowserEvents2::NewWindow2](https://msdn.microsoft.com/en-us/library/aa768287.aspx)