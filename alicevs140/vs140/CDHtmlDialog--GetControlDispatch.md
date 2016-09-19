---
title: "CDHtmlDialog::GetControlDispatch"
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
ms.assetid: 55bc8de9-93a1-48d5-ad63-8f38ddac2d10
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDHtmlDialog::GetControlDispatch
Retrieves the `IDispatch` interface on an ActiveX control embedded in the HTML document returned by [GetDHtmlDocument](../vs140/CDHtmlDialog--GetDHtmlDocument.md).  
  
## Syntax  
  
```  
  
      HRESULT GetControlDispatch(  
   LPCTSTR szId,  
   IDispatch **ppdisp   
);  
```  
  
#### Parameters  
 `szId`  
 The HTML ID of an ActiveX control.  
  
 *ppdisp*  
 The `IDispatch` interface of the control if found in the Web page.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [CDHtmlDialog Class](../vs140/CDHtmlDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDHtmlDialog::GetElement](../vs140/CDHtmlDialog--GetElement.md)   
 [CDHtmlDialog::GetElementInterface](../vs140/CDHtmlDialog--GetElementInterface.md)