---
title: "CDHtmlDialog::TranslateUrl"
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
ms.assetid: 1fae9147-a150-4f70-9c06-0cb095414871
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDHtmlDialog::TranslateUrl
Called to modify the URL to be loaded.  
  
## Syntax  
  
```  
  
      STDMETHOD(TranslateUrl)(  
   DWORD dwTranslate,  
   OLECHAR * pchURLIn,  
   OLECHAR ** ppchURLOut   
);  
```  
  
#### Parameters  
 `dwTranslate`  
 See `dwTranslate` in [IDocHostUIHandler::TranslateUrl](https://msdn.microsoft.com/en-us/library/aa753267.aspx) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `pchURLIn`  
 See `pchURLIn` in **IDocHostUIHandler::TranslateUrl** in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `ppchURLOut`  
 See `ppchURLOut` in **IDocHostUIHandler::TranslateUrl** in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 Returns **S_FALSE**.  
  
## Remarks  
 This member function is CDHtmlDialog's implementation of [IDocHostUIHandler::TranslateUrl](https://msdn.microsoft.com/en-us/library/aa753267.aspx), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [CDHtmlDialog Class](../vs140/CDHtmlDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [IDocHostUIhandler Interface](https://msdn.microsoft.com/en-us/library/aa753260.aspx)