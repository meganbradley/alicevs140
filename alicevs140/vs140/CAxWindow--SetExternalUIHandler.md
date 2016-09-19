---
title: "CAxWindow::SetExternalUIHandler"
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
ms.assetid: eeb47b39-670e-4ac4-ac08-b01f71519709
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAxWindow::SetExternalUIHandler
Sets the external [IDocHostUIHandlerDispatch](../vs140/IDocHostUIHandlerDispatch-Interface.md) interface for the `CAxWindow` object.  
  
## Syntax  
  
```  
  
      HRESULT SetExternalUIHandler(  
   IDocHostUIHandlerDispatch* pUIHandler   
);  
```  
  
#### Parameters  
 *pUIHandler*  
 [in] A pointer to an **IDocHostUIHandlerDispatch** interface.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
 The external `IDocHostUIHandlerDispatch` interface is used by controls that query the host's site for the `IDocHostUIHandlerDispatch` interface. The WebBrowser control is one control that does this.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CAxWindow Class](../vs140/CAxWindow-Class.md)   
 [CAxWindow::SetExternalDispatch](../vs140/CAxWindow--SetExternalDispatch.md)