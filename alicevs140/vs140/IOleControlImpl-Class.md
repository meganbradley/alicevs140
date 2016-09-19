---
title: "IOleControlImpl Class"
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
ms.assetid: 5a4255ad-ede4-49ca-ba9a-07c2e919fa85
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleControlImpl Class
This class provides a default implementation of the **IOleControl** interface and implements **IUnknown**.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
  
template< class  T>  
   class  
   IOleControlImpl  
  
```  
  
#### Parameters  
 `T`  
 Your class, derived from `IOleControlImpl`.  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[IOleControlImpl::FreezeEvents](../vs140/IOleControlImpl--FreezeEvents.md)|Indicates whether or not the container ignores or accepts events from the control.|  
|[IOleControlImpl::GetControlInfo](../vs140/IOleControlImpl--GetControlInfo.md)|Fills in information about the control's keyboard behavior. The ATL implementation returns **E_NOTIMPL**.|  
|[IOleControlImpl::OnAmbientPropertyChange](../vs140/IOleControlImpl--OnAmbientPropertyChange.md)|Informs a control that one or more of the container's ambient properties has changed. The ATL implementation returns `S_OK`.|  
|[IOleControlImpl::OnMnemonic](../vs140/IOleControlImpl--OnMnemonic.md)|Informs the control that a user has pressed a specified keystroke. The ATL implementation returns **E_NOTIMPL**.|  
  
## Remarks  
 Class `IOleControlImpl` provides a default implementation of the [IOleControl](http://msdn.microsoft.com/library/windows/desktop/ms694320) interface and implements **IUnknown** by sending information to the dump device in debug builds.  
  
 **Related Articles** [ATL Tutorial](../vs140/Active-Template-Library--ATL--Tutorial.md), [Creating an ATL Project](../vs140/Creating-an-ATL-Project.md)  
  
## Inheritance Hierarchy  
 `IOleControl`  
  
 `IOleControlImpl`  
  
## Requirements  
 **Header:** atlctl.h  
  
##  <a name="iolecontrolimpl__freezeevents"></a>  IOleControlImpl::FreezeEvents  
 In ATL's implementation, `FreezeEvents` increments the control class's `m_nFreezeEvents` data member if `bFreeze` is **TRUE**, and decrements `m_nFreezeEvents` if `bFreeze` is **FALSE**.  
  
```  
  
HRESULT FreezeEvents(  
      BOOL  bFreeze  
   );  
  
```  
  
### Remarks  
 `FreezeEvents` then returns `S_OK`.  
  
 See [IOleControl::FreezeEvents](http://msdn.microsoft.com/library/windows/desktop/ms678482) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
##  <a name="iolecontrolimpl__getcontrolinfo"></a>  IOleControlImpl::GetControlInfo  
 Fills in information about the control's keyboard behavior.  
  
```  
  
HRESULT GetControlInfo(  
      LPCONTROLINFO  pCI  
   );  
  
```  
  
### Remarks  
 See [IOleControl:GetControlInfo](http://msdn.microsoft.com/library/windows/desktop/ms693730) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
### Return Value  
 Returns **E_NOTIMPL**.  
  
##  <a name="iolecontrolimpl__onambientpropertychange"></a>  IOleControlImpl::OnAmbientPropertyChange  
 Informs a control that one or more of the container's ambient properties has changed.  
  
```  
  
HRESULT OnAmbientPropertyChange(  
      DISPID  dispid  
   );  
  
```  
  
### Return Value  
 Returns `S_OK`.  
  
### Remarks  
 See [IOleControl::OnAmbientPropertyChange](http://msdn.microsoft.com/library/windows/desktop/ms690175) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
##  <a name="iolecontrolimpl__onmnemonic"></a>  IOleControlImpl::OnMnemonic  
 Informs the control that a user has pressed a specified keystroke.  
  
```  
  
HRESULT OnMnemonic(  
      LPMSG  pMsg  
   );  
  
```  
  
### Return Value  
 Returns **E_NOTIMPL**.  
  
### Remarks  
 See [IOleControl::OnMnemonic](http://msdn.microsoft.com/library/windows/desktop/ms680699) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## See Also  
 [IOleObjectImpl Class](../vs140/IOleObjectImpl-Class.md)   
 [ActiveX Controls Interfaces](http://msdn.microsoft.com/library/windows/desktop/ms692724)   
 [Class Overview](../vs140/ATL-Class-Overview.md)