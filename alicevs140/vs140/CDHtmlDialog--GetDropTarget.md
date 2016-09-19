---
title: "CDHtmlDialog::GetDropTarget"
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
ms.assetid: 3da28f53-9cac-43de-8c35-b91d85dadc9a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDHtmlDialog::GetDropTarget
Called by the contained WebBrowser control when it is being used as a drop target to allow the dialog to supply an alternative [IDropTarget](http://msdn.microsoft.com/library/windows/desktop/ms679679).  
  
## Syntax  
  
```  
  
      STDMETHOD(GetDropTarget)(  
   IDropTarget *pDropTarget,  
   IDropTarget **ppDropTarget  
);  
```  
  
#### Parameters  
 `pDropTarget`  
 See `pDropTarget` in [IDocHostUIHandler::GetDropTarget](https://msdn.microsoft.com/en-us/library/aa753255.aspx) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `ppDropTarget`  
 See `ppDropTarget` in **IDocHostUIHandler::GetDropTarget** in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 Returns **E_NOTIMPL**.  
  
## Remarks  
 This member function is CDHtmlDialog's implementation of [IDocHostUIHandler::GetDropTarget](https://msdn.microsoft.com/en-us/library/aa753255.aspx), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [CDHtmlDialog Class](../vs140/CDHtmlDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [IDocHostUIhandler Interface](https://msdn.microsoft.com/en-us/library/aa753260.aspx)