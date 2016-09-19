---
title: "IAxWinAmbientDispatch Interface"
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
ms.assetid: 55ba6f7b-7a3c-4792-ae47-c8a84b683ca9
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAxWinAmbientDispatch Interface
This interface provides methods for specifying characteristics of the hosted control or container.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
  
interface IAxWinAmbientDispatch : IDispatch  
  
```  
  
## Members  
  
### Methods  
  
|||  
|-|-|  
|[get_AllowContextMenu](../vs140/IAxWinAmbientDispatch--get_AllowContextMenu.md)|The **AllowContextMenu** property specifies whether the hosted control is allowed to display its own context menu.|  
|[get_AllowShowUI](../vs140/IAxWinAmbientDispatch--get_AllowShowUI.md)|The **AllowShowUI** property specifies whether the hosted control is allowed to display its own user interface.|  
|[get_AllowWindowlessActivation](../vs140/IAxWinAmbientDispatch--get_AllowWindowlessActivation.md)|The **AllowWindowlessActivation** property specifies whether the container will allow windowless activation.|  
|[get_BackColor](../vs140/IAxWinAmbientDispatch--get_BackColor.md)|The `BackColor` property specifies the ambient background color of the container.|  
|[get_DisplayAsDefault](../vs140/IAxWinAmbientDispatch--get_DisplayAsDefault.md)|**DisplayAsDefault** is an ambient property that allows a control to find out if it is the default control.|  
|[get_DocHostDoubleClickFlags](../vs140/IAxWinAmbientDispatch--get_DocHostDoubleClickFlags.md)|The **DocHostDoubleClickFlags** property specifies the operation that should take place in response to a double-click.|  
|[get_DocHostFlags](../vs140/IAxWinAmbientDispatch--get_DocHostFlags.md)|The **DocHostFlags** property specifies the user interface capabilities of the host object.|  
|[get_Font](../vs140/IAxWinAmbientDispatch--get_Font.md)|The **Font** property specifies the ambient font of the container.|  
|[get_ForeColor](../vs140/IAxWinAmbientDispatch--get_ForeColor.md)|The `ForeColor` property specifies the ambient foreground color of the container.|  
|[get_LocaleID](../vs140/IAxWinAmbientDispatch--get_LocaleID.md)|The **LocaleID** property specifies the ambient locale ID of the container.|  
|[get_MessageReflect](../vs140/IAxWinAmbientDispatch--get_MessageReflect.md)|The **MessageReflect** ambient property specifies whether the container will reflect messages to the hosted control.|  
|[get_OptionKeyPath](../vs140/IAxWinAmbientDispatch--get_OptionKeyPath.md)|The **OptionKeyPath** property specifies the registry key path to user settings.|  
|[get_ShowGrabHandles](../vs140/IAxWinAmbientDispatch--get_ShowGrabHandles.md)|The **ShowGrabHandles** ambient property allows the control to find out if it should draw itself with grab handles.|  
|[get_ShowHatching](../vs140/IAxWinAmbientDispatch--get_ShowHatching.md)|The **ShowHatching** ambient property allows the control to find out if it should draw itself hatched.|  
|[get_UserMode](../vs140/IAxWinAmbientDispatch--get_UserMode.md)|The **UserMode** property specifies the ambient user mode of the container.|  
|[put_AllowContextMenu](../vs140/IAxWinAmbientDispatch--put_AllowContextMenu.md)|The **AllowContextMenu** property specifies whether the hosted control is allowed to display its own context menu.|  
|[put_AllowShowUI](../vs140/IAxWinAmbientDispatch--put_AllowShowUI.md)|The **AllowShowUI** property specifies whether the hosted control is allowed to display its own user interface.|  
|[put_AllowWindowlessActivation](../vs140/IAxWinAmbientDispatch--put_AllowWindowlessActivation.md)|The **AllowWindowlessActivation** property specifies whether the container will allow windowless activation.|  
|[put_BackColor](../vs140/IAxWinAmbientDispatch--put_BackColor.md)|The `BackColor` property specifies the ambient background color of the container.|  
|[put_DisplayAsDefault](../vs140/IAxWinAmbientDispatch--put_DisplayAsDefault.md)|**DisplayAsDefault** is an ambient property that allows a control to find out if it is the default control.|  
|[put_DocHostDoubleClickFlags](../vs140/IAxWinAmbientDispatch--put_DocHostDoubleClickFlags.md)|The **DocHostDoubleClickFlags** property specifies the operation that should take place in response to a double-click.|  
|[put_DocHostFlags](../vs140/IAxWinAmbientDispatch--put_DocHostFlags.md)|The **DocHostFlags** property specifies the user interface capabilities of the host object.|  
|[put_Font](../vs140/IAxWinAmbientDispatch--put_Font.md)|The **Font** property specifies the ambient font of the container.|  
|[put_ForeColor](../vs140/IAxWinAmbientDispatch--put_ForeColor.md)|The `ForeColor` property specifies the ambient foreground color of the container.|  
|[put_LocaleID](../vs140/IAxWinAmbientDispatch--put_LocaleID.md)|The **LocaleID** property specifies the ambient locale ID of the container.|  
|[put_MessageReflect](../vs140/IAxWinAmbientDispatch--put_MessageReflect.md)|The **MessageReflect** ambient property specifies whether the container will reflect messages to the hosted control.|  
|[put_OptionKeyPath](../vs140/IAxWinAmbientDispatch--put_OptionKeyPath.md)|The **OptionKeyPath** property specifies the registry key path to user settings.|  
|[put_UserMode](../vs140/IAxWinAmbientDispatch--put_UserMode.md)|The **UserMode** property specifies the ambient user mode of the container.|  
  
## Remarks  
 This interface is exposed by ATL's ActiveX control hosting objects. Call the methods on this interface to set the ambient properties available to the hosted control or to specify other aspects of the container's behavior. To supplement the properties provided by `IAxWinAmbientDispatch`, use [IAxWinAmbientDispatchEx](../vs140/IAxWinAmbientDispatchEx-Interface.md).  
  
 [AXHost](https://msdn.microsoft.com/en-us/library/system.windows.forms.axhost.aspx) will try to load type information about `IAxWinAmbientDispatch` and `IAxWinAmbientDispatchEx` from the typelib that contains the code.  
  
 If you are linking to ATL90.dll, **AXHost** will load the type information from the typelib in the DLL.  
  
 See [Hosting ActiveX Controls Using ATL AXHost](../vs140/Hosting-ActiveX-Controls-Using-ATL-AXHost.md) for more details.  
  
## Requirements  
 The definition of this interface is available in a number of forms, as shown in the table below.  
  
|Definition Type|File|  
|---------------------|----------|  
|IDL|atliface.idl|  
|Type Library|ATL.dll|  
|C++|atliface.h (also included in ATLBase.h)|  
  
## See Also  
 [IAxWinAmbientDispatchEx Interface](../vs140/IAxWinAmbientDispatchEx-Interface.md)   
 [IAxWinHostWindow Interface](../vs140/IAxWinHostWindow-Interface.md)   
 [CAxWindow::QueryHost](../vs140/CAxWindow--QueryHost.md)   
 [AtlAxGetHost](../vs140/AtlAxGetHost.md)