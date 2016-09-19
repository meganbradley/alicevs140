---
title: "What Is the ATL Control-Hosting API?"
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
ms.topic: article
ms.assetid: 75b27e45-cfba-4950-aa35-96cc7d8da753
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# What Is the ATL Control-Hosting API?
ATL's control-hosting API is the set of functions that allows any window to act as an ActiveX control container. These functions can be statically or dynamically linked into your project since they are available as source code and exposed by ATL90.dll. The control-hosting functions are listed in the table below.  
  
|Function|Description|  
|--------------|-----------------|  
|[AtlAxAttachControl](../vs140/AtlAxAttachControl.md)|Creates a host object, connects it to the supplied window, then attaches an existing control.|  
|[AtlAxCreateControl](../vs140/AtlAxCreateControl.md)|Creates a host object, connects it to the supplied window, then loads a control.|  
|[AtlAxCreateControlLic](../vs140/AtlAxCreateControlLic.md)|Creates a licensed ActiveX control, initializes it, and hosts it in the specified window, similar to [AtlAxCreateControl](../vs140/AtlAxCreateControl.md).|  
|[AtlAxCreateControlEx](../vs140/AtlAxCreateControlEx.md)|Creates a host object, connects it to the supplied window, then loads a control (also allows event sinks to be set up).|  
|[AtlAxCreateControlLicEx](../vs140/AtlAxCreateControlLicEx.md)|Creates a licensed ActiveX control, initializes it, and hosts it in the specified window, similar to [AtlAxCreateControlLic](../vs140/AtlAxCreateControlLic.md).|  
|[AtlAxCreateDialog](../vs140/AtlAxCreateDialog.md)|Creates a modeless dialog box from a dialog resource and returns the window handle.|  
|[AtlAxDialogBox](../vs140/AtlAxDialogBox.md)|Creates a modal dialog box from a dialog resource.|  
|[AtlAxGetControl](../vs140/AtlAxGetControl.md)|Returns the **IUnknown** interface pointer of the control hosted in a window.|  
|[AtlAxGetHost](../vs140/AtlAxGetHost.md)|Returns the **IUnknown** interface pointer of the host object connected to a window.|  
|[AtlAxWinInit](../vs140/AtlAxWinInit.md)|Initializes the control-hosting code.|  
|[AtlAxWinTerm](../vs140/AtlAxWinTerm.md)|Uninitializes the control-hosting code.|  
  
 The `HWND` parameters in the first three functions must be an existing window of (almost) any type. If you call any of these three functions explicitly (typically, you won't have to), do not pass a handle to a window that's already acting as a host (if you do, the existing host object won't be freed).  
  
 The first seven functions call [AtlAxWinInit](../vs140/AtlAxWinInit.md) implicitly.  
  
> [!NOTE]
>  The control-hosting API forms the foundation of ATL's support for ActiveX control containment. However, there is usually little need to call these functions directly if you take advantage of or make full use of ATL's wrapper classes. For more information, see [Which ATL Classes Facilitate ActiveX Control Containment?](../vs140/Which-ATL-Classes-Facilitate-ActiveX-Control-Containment-.md).  
  
## See Also  
 [Control Containment FAQ](../vs140/ATL-Control-Containment-FAQ.md)