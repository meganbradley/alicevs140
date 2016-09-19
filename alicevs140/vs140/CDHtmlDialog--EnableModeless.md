---
title: "CDHtmlDialog::EnableModeless"
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
ms.assetid: c1b95ed4-679c-4264-a296-2f27d37a37c7
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDHtmlDialog::EnableModeless
Enables modeless dialog boxes.  
  
## Syntax  
  
```  
  
      STDMETHOD(EnableModeless)(  
   BOOL fEnable  
);  
```  
  
#### Parameters  
 `fEnable`  
 See `fEnable` in [IDocHostUIHandler::EnableModeless](https://msdn.microsoft.com/en-us/library/aa753253.aspx) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 Returns **E_NOTIMPL**.  
  
## Remarks  
 This member function is CDHtmlDialog's implementation of [IDocHostUIHandler::EnableModeless](https://msdn.microsoft.com/en-us/library/aa753253.aspx), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [CDHtmlDialog Class](../vs140/CDHtmlDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [IDocHostUIhandler Interface](https://msdn.microsoft.com/en-us/library/aa753260.aspx)