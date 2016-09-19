---
title: "CDHtmlDialog::ResizeBorder"
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
ms.assetid: cc47056b-3223-4c18-b866-b5a622ba4f5b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDHtmlDialog::ResizeBorder
Alerts the object that it needs to resize its border space.  
  
## Syntax  
  
```  
  
      STDMETHOD(ResizeBorder)(   
   LPCRECT prcBorder,   
   IOleInPlaceUIWindow * pUIWindow,   
   BOOL fRameWindow    
);  
```  
  
#### Parameters  
 `prcBorder`  
 See `prcBorder` in [IDocHostUIHandler::ResizeBorder](https://msdn.microsoft.com/en-us/library/aa753263.aspx) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `pUIWindow`  
 See `pUIWindow` in **IDocHostUIHandler::ResizeBorder** in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `fFrameWindow`  
 See *fFrameWindow* in **IDocHostUIHandler::ResizeBorder** in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 Returns **E_NOTIMPL**.  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [CDHtmlDialog Class](../vs140/CDHtmlDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [IDocHostUIhandler Interface](https://msdn.microsoft.com/en-us/library/aa753260.aspx)