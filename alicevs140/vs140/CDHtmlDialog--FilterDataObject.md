---
title: "CDHtmlDialog::FilterDataObject"
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
ms.assetid: 40f1b9b5-2fa5-44dc-b956-5545a7878214
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDHtmlDialog::FilterDataObject
Allows the dialog to filter clipboard data objects created by the hosted browser.  
  
## Syntax  
  
```  
  
      STDMETHOD(FilterDataObject)(  
   IDataObject *pDO,  
   IDataObject **ppDORet  
);  
```  
  
#### Parameters  
 `pDO`  
 See `pDO` in [IDocHostUIHandler::FilterDataObject](https://msdn.microsoft.com/en-us/library/aa753254.aspx) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `ppDORet`  
 See `ppDORet` in **IDocHostUIHandler::FilterDataObject** in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 Returns **S_FALSE**.  
  
## Remarks  
 This member function is CDHtmlDialog's implementation of [IDocHostUIHandler::FilterDataObject](https://msdn.microsoft.com/en-us/library/aa753254.aspx), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [CDHtmlDialog Class](../vs140/CDHtmlDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [IDocHostUIhandler Interface](https://msdn.microsoft.com/en-us/library/aa753260.aspx)