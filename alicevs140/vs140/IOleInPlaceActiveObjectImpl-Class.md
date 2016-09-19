---
title: "IOleInPlaceActiveObjectImpl Class"
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
ms.assetid: 44e6cc6d-a2dc-4187-98e3-73cf0320dea9
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleInPlaceActiveObjectImpl Class
This class provides methods for assisting communication between an in-place control and its container.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
  
template< class  T>  
   class IOleInPlaceActiveObjectImpl  
  
```  
  
#### Parameters  
 `T`  
 Your class, derived from `IOleInPlaceActiveObjectImpl`.  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[IOleInPlaceActiveObjectImpl::ContextSensitiveHelp](../vs140/IOleInPlaceActiveObjectImpl--ContextSensitiveHelp.md)|Enables context-sensitive help. The ATL implementation returns **E_NOTIMPL**.|  
|[IOleInPlaceActiveObjectImpl::EnableModeless](../vs140/IOleInPlaceActiveObjectImpl--EnableModeless.md)|Enables modeless dialog boxes. The ATL implementation returns `S_OK`.|  
|[IOleInPlaceActiveObjectImpl::GetWindow](../vs140/IOleInPlaceActiveObjectImpl--GetWindow.md)|Gets a window handle.|  
|[IOleInPlaceActiveObjectImpl::OnDocWindowActivate](../vs140/IOleInPlaceActiveObjectImpl--OnDocWindowActivate.md)|Notifies the control when the container's document window is activated or deactivated. The ATL implementation returns `S_OK`.|  
|[IOleInPlaceActiveObjectImpl::OnFrameWindowActivate](../vs140/IOleInPlaceActiveObjectImpl--OnFrameWindowActivate.md)|Notifies the control when the container's top-level frame window is activated or deactivated. The ATL implementation returns|  
|[IOleInPlaceActiveObjectImpl::ResizeBorder](../vs140/IOleInPlaceActiveObjectImpl--ResizeBorder.md)|Informs the control it needs to resize its borders. The ATL implementation returns `S_OK`.|  
|[IOleInPlaceActiveObjectImpl::TranslateAccelerator](../vs140/IOleInPlaceActiveObjectImpl--TranslateAccelerator.md)|Processes menu accelerator-key messages from the container. The ATL implementation returns **E_NOTIMPL**.|  
  
## Remarks  
 The [IOleInPlaceActiveObject](http://msdn.microsoft.com/library/windows/desktop/ms691299) interface assists communication between an in-place control and its container; for example, communicating the active state of the control and container, and informing the control it needs to resize itself. Class `IOleInPlaceActiveObjectImpl` provides a default implementation of `IOleInPlaceActiveObject` and supports **IUnknown** by sending information to the dump device in debug builds.  
  
 **Related Articles** [ATL Tutorial](../vs140/Active-Template-Library--ATL--Tutorial.md), [Creating an ATL Project](../vs140/Creating-an-ATL-Project.md)  
  
## Inheritance Hierarchy  
 `IOleInPlaceActiveObject`  
  
 `IOleInPlaceActiveObjectImpl`  
  
## Requirements  
 **Header:** atlctl.h  
  
##  <a name="ioleinplaceactiveobjectimpl__contextsensitivehelp"></a>  IOleInPlaceActiveObjectImpl::ContextSensitiveHelp  
 Enables context-sensitive help.  
  
```  
  
HRESULT ContextSensitiveHelp(  
      BOOL  fEnterMode  
   );  
  
```  
  
### Return Value  
 Returns **E_NOTIMPL**.  
  
### Remarks  
 See [IOleWindow::ContextSensitiveHelp](http://msdn.microsoft.com/library/windows/desktop/ms680059) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
##  <a name="ioleinplaceactiveobjectimpl__enablemodeless"></a>  IOleInPlaceActiveObjectImpl::EnableModeless  
 Enables modeless dialog boxes.  
  
```  
  
HRESULT EnableModeless(  
      BOOL  fEnable  
   );  
  
```  
  
### Return Value  
 Returns `S_OK`.  
  
### Remarks  
 See [IOleInPlaceActiveObject::EnableModeless](http://msdn.microsoft.com/library/windows/desktop/ms680115) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
##  <a name="ioleinplaceactiveobjectimpl__getwindow"></a>  IOleInPlaceActiveObjectImpl::GetWindow  
 The container calls this function to get the window handle of the control.  
  
```  
  
HRESULT GetWindow(  
      HWND*  phwnd  
   );  
  
```  
  
### Remarks  
 Some containers will not work with a control that has been windowless, even if it is currently windowed. In ATL's implementation, if the **CComControl::m_bWasOnceWindowless** data member is **TRUE**, the function returns **E_FAIL**. Otherwise, if \* *phwnd* is not **NULL**, `GetWindow` assigns *phwnd* to the control class's data member `m_hWnd` and returns `S_OK`.  
  
 See [IOleWindow::GetWindow](http://msdn.microsoft.com/library/windows/desktop/ms687282) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
##  <a name="ioleinplaceactiveobjectimpl__ondocwindowactivate"></a>  IOleInPlaceActiveObjectImpl::OnDocWindowActivate  
 Notifies the control when the container's document window is activated or deactivated.  
  
```  
  
HRESULT OnDocWindowActivate(  
      BOOL  fActivate  
   );  
  
```  
  
### Return Value  
 Returns `S_OK`.  
  
### Remarks  
 See [IOleInPlaceActiveObject::OnDocWindowActivate](http://msdn.microsoft.com/library/windows/desktop/ms687281) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
##  <a name="ioleinplaceactiveobjectimpl__onframewindowactivate"></a>  IOleInPlaceActiveObjectImpl::OnFrameWindowActivate  
 Notifies the control when the container's top-level frame window is activated or deactivated.  
  
```  
  
HRESULT OnFrameWindowActivate(  
      BOOL  fActivate  
   );  
  
```  
  
### Return Value  
 Returns `S_OK`.  
  
### Remarks  
 See [IOleInPlaceActiveObject::OnFrameWindowActivate](http://msdn.microsoft.com/library/windows/desktop/ms683969) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
##  <a name="ioleinplaceactiveobjectimpl__resizeborder"></a>  IOleInPlaceActiveObjectImpl::ResizeBorder  
 Informs the control it needs to resize its borders.  
  
```  
  
HRESULT ResizeBorder(  
      LPRECT  prcBorder,  
      IOleInPlaceUIWindow*  pUIWindow,  
      BOOL  fFrameWindow  
   );  
  
```  
  
### Return Value  
 Returns `S_OK`.  
  
### Remarks  
 See [IOleInPlaceActiveObject::ResizeBorder](http://msdn.microsoft.com/library/windows/desktop/ms680053) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
##  <a name="ioleinplaceactiveobjectimpl__translateaccelerator"></a>  IOleInPlaceActiveObjectImpl::TranslateAccelerator  
 Processes menu accelerator-key messages from the container.  
  
```  
  
HRESULT TranslateAccelerator(  
      LPMSG  lpmsg  
   );  
  
```  
  
### Return Value  
 This method supports the following return values:  
  
 `S_OK` if the message was translated successfully.  
  
 **S_FALSE** if the message was not translated.  
  
### Remarks  
 See [IOleInPlaceActiveObject::TranslateAccelerator](http://msdn.microsoft.com/library/windows/desktop/ms693360) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## See Also  
 [CComControl Class](../vs140/CComControl-Class.md)   
 [ActiveX Controls Interfaces](http://msdn.microsoft.com/library/windows/desktop/ms692724)   
 [Class Overview](../vs140/ATL-Class-Overview.md)