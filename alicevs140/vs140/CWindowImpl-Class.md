---
title: "CWindowImpl Class"
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
ms.assetid: 02eefd45-a0a6-4d1b-99f6-dbf627e2cc2f
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindowImpl Class
Provides methods for creating or subclassing a window.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
  
template <  
   class  T,  
   class  TBase  
   = CWindow,  
   class  TWinTraits  
   = CControlWinTraits >  
   class ATL_NO_VTABLE CWindowImpl :  
   public CWindowImplBaseT<  TBase, TWinTraits>  
  
```  
  
#### Parameters  
 `T`  
 Your new class, derived from `CWindowImpl`.  
  
 *TBase*  
 The base class of your class. By default, the base class is [CWindow](../vs140/CWindow-Class.md).  
  
 `TWinTraits`  
 A [traits class](../vs140/Understanding-Window-Traits.md) that defines styles for your window. The default is `CControlWinTraits`.  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CWindowImpl::Create](../vs140/CWindowImpl--Create.md)|Creates a window.|  
  
### CWindowImplBaseT Methods  
  
|||  
|-|-|  
|[DefWindowProc](../vs140/CWindowImpl--DefWindowProc.md)|Provides default message processing.|  
|[GetCurrentMessage](../vs140/CWindowImpl--GetCurrentMessage.md)|Returns the current message.|  
|[GetWindowProc](../vs140/CWindowImpl--GetWindowProc.md)|Returns the current window procedure.|  
|[OnFinalMessage](../vs140/CWindowImpl--OnFinalMessage.md)|Called after the last message is received (typically `WM_NCDESTROY`).|  
|[SubclassWindow](../vs140/CWindowImpl--SubclassWindow.md)|Subclasses a window.|  
|[UnsubclassWindow](../vs140/CWindowImpl--UnsubclassWindow.md)|Restores a previously subclassed window.|  
  
### Static Methods  
  
|||  
|-|-|  
|[GetWndClassInfo](../vs140/CWindowImpl--GetWndClassInfo.md)|Returns a static instance of [CWndClassInfo](../vs140/CWndClassInfo-Class.md), which manages the window class information.|  
|[WindowProc](../vs140/CWindowImpl--WindowProc.md)|Processes messages sent to the window.|  
  
### Data Members  
  
|||  
|-|-|  
|[m_pfnSuperWindowProc](../vs140/CWindowImpl--m_pfnSuperWindowProc.md)|Points to the window class's original window procedure.|  
  
## Remarks  
 You can use `CWindowImpl` to create a window or subclass an existing window. the `CWindowImpl` window procedure uses a message map to direct messages to the appropriate handlers.  
  
 `CWindowImpl::Create` creates a window based on the window class information that's managed by [CWndClassInfo](../vs140/CWndClassInfo-Class.md). `CWindowImpl` contains the [DECLARE_WND_CLASS](../vs140/DECLARE_WND_CLASS.md) macro, which means `CWndClassInfo` registers a new window class. If you want to superclass an existing window class, derive your class from `CWindowImpl` and include the [DECLARE_WND_SUPERCLASS](../vs140/DECLARE_WND_SUPERCLASS.md) macro. In this case, `CWndClassInfo` registers a window class that's based on an existing class but uses `CWindowImpl::WindowProc`. For example:  
  
 [!CODE [NVC_ATL_Windowing#43](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#43)]  
  
> [!NOTE]
>  Because `CWndClassInfo` manages the information for just one window class, each window created through an instance of `CWindowImpl` is based on the same window class.  
  
 `CWindowImpl` also supports window subclassing. The `SubclassWindow` method attaches an existing window to the `CWindowImpl` object and changes the window procedure to `CWindowImpl::WindowProc`. Each instance of `CWindowImpl` can subclass a different window.  
  
> [!NOTE]
>  For any given `CWindowImpl` object, call either **Create** or `SubclassWindow`. Don't invoke both methods on the same object.  
  
 In addition to `CWindowImpl`, ATL provides [CContainedWindow](../vs140/CContainedWindowT-Class.md) to create a window that's contained in another object.  
  
 The base class destructor (~                **CWindowImplRoot**) ensures that the window is gone before the object is destroyed.  
  
 `CWindowImpl` derives from **CWindowImplBaseT**, which derives from **CWindowImplRoot**, which derives from **TBase** and [CMessageMap](../vs140/CMessageMap-Class.md).  
  
|For more information about|See|  
|--------------------------------|---------|  
|Creating controls|[ATL Tutorial](../vs140/Active-Template-Library--ATL--Tutorial.md)|  
|Using windows in ATL|[ATL Window Classes](../vs140/ATL-Window-Classes.md)|  
|ATL Project Wizard|[Creating an ATL Project](../vs140/Creating-an-ATL-Project.md)|  
  
## Inheritance Hierarchy  
 [CMessageMap](../vs140/CMessageMap-Class.md)  
  
 `TBase`  
  
 `CWindowImplRoot`  
  
 `CWindowImplBaseT`  
  
 `CWindowImpl`  
  
## Requirements  
 **Header:** atlwin.h  
  
##  <a name="cwindowimpl__create"></a>  CWindowImpl::Create  
 Creates a window based on a new window class.  
  
```  
  
HWND Create(  
      HWND  hWndParent,  
      _U_RECT  rect  
    = NULL,  
      LPCTSTR  szWindowName  
    = NULL,  
      DWORD  dwStyle  
    = 0,  
      DWORD  dwExStyle  
    = 0,  
      _U_MENUorID  MenuOrID  
    = 0U,  
      LPVOID  lpCreateParam  
    = NULL  
   );  
  
```  
  
### Parameters  
 `hWndParent`  
 [in] The handle to the parent or owner window.  
  
 `rect`  
 [in] A [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) structure specifying the position of the window. The `RECT` can be passed by pointer or by reference.  
  
 `szWindowName`  
 [in] Specifies the name of the window. The default value is **NULL**.  
  
 `dwStyle`  
 [in] The style of the window. This value is combined with the style provided by the traits class for the window. The default value gives the traits class full control over the style. For a list of possible values, see [CreateWindow](http://msdn.microsoft.com/library/windows/desktop/ms632679) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `dwExStyle`  
 [in] The extended window style. This value is combined with the style provided by the traits class for the window. The default value gives the traits class full control over the style. For a list of possible values, see [CreateWindowEx](http://msdn.microsoft.com/library/windows/desktop/ms632680) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `MenuOrID`  
 [in] For a child window, the window identifier. For a top-level window, a menu handle for the window. The default value is **0U**.  
  
 `lpCreateParam`  
 [in] A pointer to window-creation data. For a full description, see the description for the final parameter to [CreateWindowEx](http://msdn.microsoft.com/library/windows/desktop/ms632680).  
  
### Return Value  
 If successful, the handle to the newly created window. Otherwise,                         **NULL**.  
  
### Remarks  
 **Create** first registers the window class if it has not yet been registered. The newly created window is automatically attached to the `CWindowImpl` object.  
  
> [!NOTE]
>  Do not call **Create** if you have already called [SubclassWindow](../vs140/CWindowImpl--SubclassWindow.md).  
  
 To use a window class that is based on an existing window class, derive your class from `CWindowImpl` and include the [DECLARE_WND_SUPERCLASS](../vs140/DECLARE_WND_SUPERCLASS.md) macro. The existing window class's window procedure is saved in [m_pfnSuperWindowProc](../vs140/CWindowImpl--m_pfnSuperWindowProc.md). For more information, see the [CWindowImpl](../vs140/CWindowImpl-Class.md) overview.  
  
> [!NOTE]
>  If 0 is used as the value for the `MenuOrID` parameter, it must be specified as 0U (the default value) to avoid a compiler error.  
  
##  <a name="cwindowimpl__defwindowproc"></a>  CWindowImpl::DefWindowProc  
 Called by [WindowProc](../vs140/CWindowImpl--WindowProc.md) to process messages not handled by the message map.  
  
```  
  
LRESULT DefWindowProc(  
      UINT  uMsg,  
      WPARAM  wParam,  
      LPARAM  lParam  
   );  
   LRESULT DefWindowProc( );  
  
```  
  
### Parameters  
 `uMsg`  
 [in] The message sent to the window.  
  
 `wParam`  
 [in] Additional message-specific information.  
  
 `lParam`  
 [in] Additional message-specific information.  
  
### Return Value  
 The result of the message processing.  
  
### Remarks  
 By default, `DefWindowProc` calls the [CallWindowProc](http://msdn.microsoft.com/library/windows/desktop/ms633571) Win32 function to send the message information to the window procedure specified in [m_pfnSuperWindowProc](../vs140/CWindowImpl--m_pfnSuperWindowProc.md).  
  
 The function with no parameters automatically retrieves the needed parameters from the current message.  
  
##  <a name="cwindowimpl__getcurrentmessage"></a>  CWindowImpl::GetCurrentMessage  
 Returns the current message, packaged in the `MSG` structure.  
  
```  
  
const MSG* GetCurrentMessage( );  
  
```  
  
### Return Value  
 The current message.  
  
##  <a name="cwindowimpl__getwindowproc"></a>  CWindowImpl::GetWindowProc  
 Returns `WindowProc`, the current window procedure.  
  
```  
  
virtual WNDPROC GetWindowProc( );  
  
```  
  
### Return Value  
 The current window procedure.  
  
### Remarks  
 Override this method to replace the window procedure with your own.  
  
##  <a name="cwindowimpl__getwndclassinfo"></a>  CWindowImpl::GetWndClassInfo  
 Called by [Create](../vs140/CWindowImpl--Create.md) to access the window class information.  
  
```  
  
static CWndClassInfo& GetWndClassInfo( );  
  
```  
  
### Return Value  
 A static instance of [CWndClassInfo](../vs140/CWndClassInfo-Class.md).  
  
### Remarks  
 By default, `CWindowImpl` obtains this method through the [DECLARE_WND_CLASS](../vs140/DECLARE_WND_CLASS.md) macro, which specifies a new window class.  
  
 To superclass an existing window class, derive your class from `CWindowImpl` and include the [DECLARE_WND_SUPERCLASS](../vs140/DECLARE_WND_SUPERCLASS.md) macro to override `GetWndClassInfo`. For more information, see the [CWindowImpl](../vs140/CWindowImpl-Class.md) overview.  
  
 Besides using the `DECLARE_WND_CLASS` and `DECLARE_WND_SUPERCLASS` macros, you can override `GetWndClassInfo` with your own implementation.  
  
##  <a name="cwindowimpl__m_pfnsuperwindowproc"></a>  CWindowImpl::m_pfnSuperWindowProc  
 Depending on the window, points to one of the following window procedures.  
  
```  
  
WNDPROC m_pfnSuperWindowProc;  
  
```  
  
### Remarks  
  
|Type of window|Window procedure|  
|--------------------|----------------------|  
|A window based on a new window class, specified through the [DECLARE_WND_CLASS](../vs140/DECLARE_WND_CLASS.md) macro.|The [DefWindowProc](http://msdn.microsoft.com/library/windows/desktop/ms633572) Win32 function.|  
|A window based on a window class that modifies an existing class, specified through the [DECLARE_WND_SUPERCLASS](../vs140/DECLARE_WND_SUPERCLASS.md) macro.|The existing window class's window procedure.|  
|A subclassed window.|The subclassed window's original window procedure.|  
  
 [CWindowImpl::DefWindowProc](../vs140/CWindowImpl--DefWindowProc.md) sends message information to the window procedure saved in `m_pfnSuperWindowProc`.  
  
##  <a name="cwindowimpl__onfinalmessage"></a>  CWindowImpl::OnFinalMessage  
 Called after receiving the last message (typically `WM_NCDESTROY`).  
  
```  
  
virtual void OnFinalMessage(  
      HWND  hWnd  
   );  
  
```  
  
### Parameters  
 `hWnd`  
 [in] A handle to the window being destroyed.  
  
### Remarks  
 The default implementation of `OnFinalMessage` does nothing, but you can override this function to handle cleanup before destroying a window. If you want to automatically delete your object upon the window destruction, you can call `delete this;` in this function.  
  
##  <a name="cwindowimpl__subclasswindow"></a>  CWindowImpl::SubclassWindow  
 Subclasses the window identified by `hWnd` and attaches it to the `CWindowImpl` object.  
  
```  
  
BOOL SubclassWindow(  
      HWND  hWnd  
   );  
  
```  
  
### Parameters  
 `hWnd`  
 [in] The handle to the window being subclassed.  
  
### Return Value  
 **TRUE** if the window is successfully subclassed; otherwise,                         **FALSE**.  
  
### Remarks  
 The subclassed window now uses [CWindowImpl::WindowProc](../vs140/CWindowImpl--WindowProc.md). The original window procedure is saved in [m_pfnSuperWindowProc](../vs140/CWindowImpl--m_pfnSuperWindowProc.md).  
  
> [!NOTE]
>  Do not call `SubclassWindow` if you have already called [Create](../vs140/CWindowImpl--Create.md).  
  
##  <a name="cwindowimpl__unsubclasswindow"></a>  CWindowImpl::UnsubclassWindow  
 Detaches the subclassed window from the `CWindowImpl` object and restores the original window procedure, saved in [m_pfnSuperWindowProc](../vs140/CWindowImpl--m_pfnSuperWindowProc.md).  
  
```  
  
HWND UnsubclassWindow( );  
  
```  
  
### Return Value  
 The handle to the window previously subclassed.  
  
##  <a name="cwindowimpl__windowproc"></a>  CWindowImpl::WindowProc  
 This static function implements the window procedure.  
  
```  
  
static LRESULT CALLBACK WindowProc(  
      HWND  hWnd,  
      UINT  uMsg,  
      WPARAM  wParam,  
      LPARAM  lParam  
   );  
  
```  
  
### Parameters  
 `hWnd`  
 [in] The handle to the window.  
  
 `uMsg`  
 [in] The message sent to the window.  
  
 `wParam`  
 [in] Additional message-specific information.  
  
 `lParam`  
 [in] Additional message-specific information.  
  
### Return Value  
 The result of the message processing.  
  
### Remarks  
 `WindowProc` uses the default message map (declared with [BEGIN_MSG_MAP](../vs140/BEGIN_MSG_MAP.md)) to direct messages to the appropriate handlers. If necessary, `WindowProc` calls [DefWindowProc](../vs140/CWindowImpl--DefWindowProc.md) for additional message processing. If the final message is not handled, `WindowProc` does the following:  
  
-   Performs unsubclassing if the window was unsubclassed.  
  
-   Clears `m_hWnd`.  
  
-   Calls [OnFinalMessage](../vs140/CWindowImpl--OnFinalMessage.md) before the window is destroyed.  
  
 You can override `WindowProc` to provide a different mechanism for handling messages.  
  
## See Also  
 [BEGIN_MSG_MAP](../vs140/BEGIN_MSG_MAP.md)   
 [CComControl Class](../vs140/CComControl-Class.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)