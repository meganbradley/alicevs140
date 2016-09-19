---
title: "IAxWinHostWindow Interface"
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
ms.assetid: 9821c035-cd52-4c46-b58a-9278064f09b4
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAxWinHostWindow Interface
This interface provides methods for manipulating a control and its host object.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
  
interface IAxWinHostWindow : IUnknown  
  
```  
  
## Members  
  
### Methods  
  
|||  
|-|-|  
|[AttachControl](../vs140/IAxWinHostWindow--AttachControl.md)|Attaches an existing control to the host object.|  
|[CreateControl](../vs140/IAxWinHostWindow--CreateControl.md)|Creates a control and attaches it to the host object.|  
|[CreateControlEx](../vs140/IAxWinHostWindow--CreateControlEx.md)|Creates a control, attaches it to the host object, and optionally sets up an event handler.|  
|[QueryControl](../vs140/IAxWinHostWindow--QueryControl.md)|Returns an interface pointer to the hosted control.|  
|[SetExternalDispatch](../vs140/IAxWinHostWindow--SetExternalDispatch.md)|Sets the external `IDispatch` interface.|  
|[SetExternalUIHandler](../vs140/IAxWinHostWindow--SetExternalUIHandler.md)|Sets the external `IDocHostUIHandlerDispatch` interface.|  
  
## Remarks  
 This interface is exposed by ATL's ActiveX control hosting objects. Call the methods on this interface to create and/or attach a control to the host object, to get an interface from a hosted control, or to set the external dispinterface or UI handler for use when hosting the Web browser.  
  
## Requirements  
 The definition of this interface is available as IDL or C++, as shown below.  
  
|Definition type|File|  
|---------------------|----------|  
|IDL|ATLIFace.idl|  
|C++|ATLIFace.h (also included in ATLBase.h)|  
  
## See Also  
 [IAxWinAmbientDispatch Interface](../vs140/IAxWinAmbientDispatch-Interface.md)   
 [CAxWindow::QueryHost](../vs140/CAxWindow--QueryHost.md)   
 [AtlAxGetHost](../vs140/AtlAxGetHost.md)