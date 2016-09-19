---
title: "CDHtmlDialog::ShowUI"
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
ms.assetid: e1506ebc-3b71-4cb8-818f-2f4db8a0037f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDHtmlDialog::ShowUI
Shows the host's UI.  
  
## Syntax  
  
```  
  
      STDMETHOD(ShowUI)(  
   DWORD dwID,  
   IOleInPlaceActiveObject * pActiveObject,  
   IOleCommandTarget * pCommandTarget,  
   IOleInPlaceFrame * pFrame,  
   IOleInPlaceUIWindow * pDoc   
);  
```  
  
#### Parameters  
 `dwID`  
 See `dwID` in [IDocHostUIHandler::ShowUI](https://msdn.microsoft.com/en-us/library/aa753265.aspx) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `pActiveObject`  
 See *d pActiveObject* in **IDocHostUIHandler::ShowUI** in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `pCommandTarget`  
 See `pCommandTarget` in **IDocHostUIHandler::ShowUI** in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `pFrame`  
 See `pFrame` in **IDocHostUIHandler::ShowUI** in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `pDoc`  
 See `pDoc` in **IDocHostUIHandler::ShowUI** in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 Returns **S_FALSE**.  
  
## Remarks  
 This member function is CDHtmlDialog's implementation of [IDocHostUIHandler::ShowUI](https://msdn.microsoft.com/en-us/library/aa753265.aspx), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [CDHtmlDialog Class](../vs140/CDHtmlDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [IDocHostUIhandler Interface](https://msdn.microsoft.com/en-us/library/aa753260.aspx)   
 [CDHtmlDialog::HideUI](../vs140/CDHtmlDialog--HideUI.md)