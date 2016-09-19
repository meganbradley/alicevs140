---
title: "CDHtmlDialog::OnFrameWindowActivate"
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
ms.assetid: 5307e1f3-59dd-4b61-ab07-d08382eb2a5d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDHtmlDialog::OnFrameWindowActivate
Called by the framework when the frame window is activated or deactivated.  
  
## Syntax  
  
```  
  
      STDMETHOD(OnFrameWindowActivate)(  
   BOOL fActivate   
);  
```  
  
#### Parameters  
 `fActivate`  
 See `fActivate` in [IDocHostUIHandler::OnFrameWindowActivate](https://msdn.microsoft.com/en-us/library/aa753262.aspx) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 Returns **E_NOTIMPL**.  
  
## Remarks  
 This member function is CDHtmlDialog's implementation of [IDocHostUIHandler::OnFrameWindowActivate](https://msdn.microsoft.com/en-us/library/aa753262.aspx), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [CDHtmlDialog Class](../vs140/CDHtmlDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [IDocHostUIhandler Interface](https://msdn.microsoft.com/en-us/library/aa753260.aspx)