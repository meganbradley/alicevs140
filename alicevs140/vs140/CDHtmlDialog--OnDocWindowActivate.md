---
title: "CDHtmlDialog::OnDocWindowActivate"
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
ms.assetid: 7c96fa16-2cb1-4dc8-93e6-ab983da5e407
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDHtmlDialog::OnDocWindowActivate
Called by the framework when the document window is activated or deactivated.  
  
## Syntax  
  
```  
  
      STDMETHOD(OnDocWindowActivate)(  
   BOOL fActivate   
);  
```  
  
#### Parameters  
 `fActivate`  
 See `fActivate` in [IDocHostUIHandler::OnDocWindowActivate](https://msdn.microsoft.com/en-us/library/aa753261.aspx) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 Returns **E_NOTIMPL**.  
  
## Remarks  
 This member function is CDHtmlDialog's implemention of [IDocHostUIHandler::OnDocWindowActivate](https://msdn.microsoft.com/en-us/library/aa753261.aspx), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [CDHtmlDialog Class](../vs140/CDHtmlDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [IDocHostUIhandler Interface](https://msdn.microsoft.com/en-us/library/aa753260.aspx)