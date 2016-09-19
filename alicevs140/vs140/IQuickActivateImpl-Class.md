---
title: "IQuickActivateImpl Class"
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
ms.assetid: aa80c056-1041-494e-b21d-2acca7dc27ea
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IQuickActivateImpl Class
This class combines containers' control initialization into a single call.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
  
template<   
   class  T>  
   class ATL_NO_VTABLE IQuickActivateImpl :  
   public IQuickActivate  
  
```  
  
#### Parameters  
 `T`  
 Your class, derived from `IQuickActivateImpl`.  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[IQuickActivateImpl::GetContentExtent](../vs140/IQuickActivateImpl--GetContentExtent.md)|Retrieves the current display size for a running control.|  
|[IQuickActivateImpl::QuickActivate](../vs140/IQuickActivateImpl--QuickActivate.md)|Performs quick initialization of controls being loaded.|  
|[IQuickActivateImpl::SetContentExtent](../vs140/IQuickActivateImpl--SetContentExtent.md)|Informs the control of how much display space the container has assigned to it.|  
  
## Remarks  
 The [IQuickActivate](http://msdn.microsoft.com/library/windows/desktop/ms690146) interface helps containers avoid delays when loading controls by combining initialization in a single call. The `QuickActivate` method allows the container to pass a pointer to a [QACONTAINER](http://msdn.microsoft.com/library/windows/desktop/ms688630) structure that holds pointers to all the interfaces the control needs. On return, the control passes back a pointer to a [QACONTROL](http://msdn.microsoft.com/library/windows/desktop/ms693721) structure that holds pointers to its own interfaces, which are used by the container. Class `IQuickActivateImpl` provides a default implementation of **IQuickActivate** and implements **IUnknown** by sending information to the dump device in debug builds.  
  
 **Related Articles** [ATL Tutorial](../vs140/Active-Template-Library--ATL--Tutorial.md), [Creating an ATL Project](../vs140/Creating-an-ATL-Project.md)  
  
## Inheritance Hierarchy  
 `IQuickActivate`  
  
 `IQuickActivateImpl`  
  
## Requirements  
 **Header:** atlctl.h  
  
##  <a name="iquickactivateimpl__getcontentextent"></a>  IQuickActivateImpl::GetContentExtent  
 Retrieves the current display size for a running control.  
  
```  
  
STDMETHOD(GetContentExtent)(  
      LPSIZEL  pSize  
   );  
  
```  
  
### Remarks  
 The size is for a full rendering of the control and is specified in HIMETRIC units.  
  
 See [IQuickActivate::GetContentExtent](http://msdn.microsoft.com/library/windows/desktop/ms693792) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
##  <a name="iquickactivateimpl__quickactivate"></a>  IQuickActivateImpl::QuickActivate  
 Performs quick initialization of controls being loaded.  
  
```  
  
STDMETHOD(QuickActivate)(  
      QACONTAINER*  pQACont,  
   QACONTROL*  pQACtrl  
   );  
  
```  
  
### Remarks  
 The structure contains pointers to interfaces needed by the control and the values of some ambient properties. Upon return, the control passes a pointer to a [QACONTROL](http://msdn.microsoft.com/library/windows/desktop/ms693721) structure that contains pointers to its own interfaces that the container requires, and additional status information.  
  
 See [IQuickActivate::QuickActivate](http://msdn.microsoft.com/library/windows/desktop/ms682421) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
##  <a name="iquickactivateimpl__setcontentextent"></a>  IQuickActivateImpl::SetContentExtent  
 Informs the control of how much display space the container has assigned to it.  
  
```  
  
STDMETHOD(SetContentExtent)(  
      LPSIZEL  pSize  
   );  
  
```  
  
### Remarks  
 The size is specified in HIMETRIC units.  
  
 See [IQuickActivate::SetContentExtent](http://msdn.microsoft.com/library/windows/desktop/ms678806) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## See Also  
 [CComControl Class](../vs140/CComControl-Class.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)