---
title: "CAtlExeModuleT Class"
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
ms.assetid: 82245f3d-91d4-44fa-aa86-7cc7fbd758d9
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlExeModuleT Class
This class represents the module for an application.  
  
## Syntax  
  
```  
  
template <class T>  
   class ATL_NO_VTABLE CAtlExeModuleT :  
      public CAtlModuleT<  T>  
  
```  
  
#### Parameters  
 `T`  
 Your class derived from `CAtlExeModuleT`.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CAtlExeModuleT::CAtlExeModuleT](../vs140/CAtlExeModuleT--CAtlExeModuleT.md)|The constructor.|  
|[CAtlExeModuleT::~CAtlExeModuleT](../vs140/CAtlExeModuleT--~CAtlExeModuleT.md)|The destructor.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CAtlExeModuleT::InitializeCom](../vs140/CAtlExeModuleT--InitializeCom.md)|Initializes COM.|  
|[CAtlExeModuleT::ParseCommandLine](../vs140/CAtlExeModuleT--ParseCommandLine.md)|Parses the command line and performs registration if necessary.|  
|[CAtlExeModuleT::PostMessageLoop](../vs140/CAtlExeModuleT--PostMessageLoop.md)|This method is called immediately after the message loop exits.|  
|[CAtlExeModuleT::PreMessageLoop](../vs140/CAtlExeModuleT--PreMessageLoop.md)|This method is called immediately before entering the message loop.|  
|[CAtlExeModuleT::RegisterClassObjects](../vs140/CAtlExeModuleT--RegisterClassObjects.md)|Registers the class object.|  
|[CAtlExeModuleT::RevokeClassObjects](../vs140/CAtlExeModuleT--RevokeClassObjects.md)|Revokes the class object.|  
|[CAtlExeModuleT::Run](../vs140/CAtlExeModuleT--Run.md)|This method executes code in the EXE module to initialize, run the message loop, and clean up.|  
|[CAtlExeModuleT::RunMessageLoop](../vs140/CAtlExeModuleT--RunMessageLoop.md)|This method executes the message loop.|  
|[CAtlExeModuleT::UninitializeCom](../vs140/CAtlExeModuleT--UninitializeCom.md)|Uninitializes COM.|  
|[CAtlExeModuleT::Unlock](../vs140/CAtlExeModuleT--Unlock.md)|Decrements the module's lock count.|  
|[CAtlExeModuleT::WinMain](../vs140/CAtlExeModuleT--WinMain.md)|This method implements the code required to run an EXE.|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CAtlExeModuleT::m_bDelayShutdown](../vs140/CAtlExeModuleT--m_bDelayShutdown.md)|A flag indicating that there should be a delay shutting down the module.|  
|[CAtlExeModuleT::m_dwPause](../vs140/CAtlExeModuleT--m_dwPause.md)|A pause value used to ensure all objects are released before shutdown.|  
|[CAtlExeModuleT::m_dwTimeOut](../vs140/CAtlExeModuleT--m_dwTimeOut.md)|A time-out value used to delay the unloading of the module.|  
  
## Remarks  
 `CAtlExeModuleT` represents the module for an application (EXE) and contains code that supports creating an EXE, processing the command line, registering class objects, running the message loop, and cleaning up on exit.  
  
 This class is designed to improve performance when COM objects in the EXE server are continually created and destroyed. After the last COM object is released, the EXE waits for a duration specified by the [CAtlExeModuleT::m_dwTimeOut](../vs140/CAtlExeModuleT--m_dwTimeOut.md) data member. If there is no activity during this period (that is, no COM objects are created), the shutdown process is initiated.  
  
 The [CAtlExeModuleT::m_bDelayShutdown](../vs140/CAtlExeModuleT--m_bDelayShutdown.md) data member is a flag used to determine if the EXE should use the mechanism defined above. If it is set to false, then the module will terminate immediately.  
  
 For more information on modules in ATL, see [ATL Module Classes](../vs140/ATL-Module-Classes.md).  
  
## Inheritance Hierarchy  
 [_ATL_MODULE](../vs140/_ATL_MODULE.md)  
  
 [CAtlModule](../vs140/CAtlModule-Class.md)  
  
 [CAtlModuleT](../vs140/CAtlModuleT-Class.md)  
  
 `CAtlExeModuleT`  
  
## Requirements  
 **Header:** atlbase.h  
  
##  <a name="catlexemodulet__catlexemodulet"></a>  CAtlExeModuleT::CAtlExeModuleT  
 The constructor.  
  
```  
  
CAtlExeModuleT( ) throw( );  
  
```  
  
### Remarks  
 If the EXE module could not be initialized, WinMain will immediately return without further processing.  
  
##  <a name="catlexemodulet___dtorcatlexemodulet"></a>  CAtlExeModuleT::~CAtlExeModuleT  
 The destructor.  
  
```  
  
~CAtlExeModuleT( ) throw( );  
  
```  
  
### Remarks  
 Frees all allocated resources.  
  
##  <a name="catlexemodulet__initializecom"></a>  CAtlExeModuleT::InitializeCom  
 Initializes COM.  
  
```  
  
static HRESULT InitializeCom( ) throw( );  
  
```  
  
### Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
### Remarks  
 This method is called from the constructor and can be overridden to initialize COM in a manner different from the default implementation. The default implementation either calls **CoInitializeEx(NULL, COINIT_MULTITHREADED)** or **CoInitialize(NULL)** depending on the project configuration.  
  
 Overriding this method normally requires overriding [CAtlExeModuleT::UninitializeCom](../vs140/CAtlExeModuleT--UninitializeCom.md).  
  
##  <a name="catlexemodulet__m_bdelayshutdown"></a>  CAtlExeModuleT::m_bDelayShutdown  
 A flag indicating that there should be a delay shutting down the module.  
  
```  
  
bool m_bDelayShutdown;  
  
```  
  
### Remarks  
 See the [CAtlExeModuleT Overview](../vs140/CAtlExeModuleT-Class.md) for details.  
  
##  <a name="catlexemodulet__m_dwpause"></a>  CAtlExeModuleT::m_dwPause  
 A pause value used to ensure all objects are gone before shutdown.  
  
```  
  
DWORD m_dwPause;  
  
```  
  
### Remarks  
 Change this value after calling [CAtlExeModuleT::InitializeCom](../vs140/CAtlExeModuleT--InitializeCom.md) to set the number of milliseconds used as the pause value for shutting down the server. The default value is 1000 milliseconds.  
  
##  <a name="catlexemodulet__m_dwtimeout"></a>  CAtlExeModuleT::m_dwTimeOut  
 A time-out value used to delay the unloading of the module.  
  
```  
  
DWORD m_dwTimeOut;  
  
```  
  
### Remarks  
 Change this value after calling [CAtlExeModuleT::InitializeCom](../vs140/CAtlExeModuleT--InitializeCom.md) to define the number of milliseconds used as the time-out value for shutting down the server. The default value is 5000 milliseconds. See the [CAtlExeModuleT Overview](../vs140/CAtlExeModuleT-Class.md) for more details.  
  
##  <a name="catlexemodulet__parsecommandline"></a>  CAtlExeModuleT::ParseCommandLine  
 Parses the command line and performs registration if necessary.  
  
```  
  
bool ParseCommandLine(  
      LPCTSTR  lpCmdLine,  
      HRESULT*  pnRetCode  
   ) throw( );  
  
```  
  
### Parameters  
 `lpCmdLine`  
 The command line passed to the application.  
  
 `pnRetCode`  
 The HRESULT corresponding to the registration (if it took place).  
  
### Return Value  
 Return true if the application should continue to run, otherwise false.  
  
### Remarks  
 This method is called from [CAtlExeModuleT::WinMain](../vs140/CAtlExeModuleT--WinMain.md) and can be overridden to handle command-line switches. The default implementation checks for **/RegServer** and **/UnRegServer** command-line arguments and performs registration or unregistration.  
  
##  <a name="catlexemodulet__postmessageloop"></a>  CAtlExeModuleT::PostMessageLoop  
 This method is called immediately after the message loop exits.  
  
```  
  
HRESULT PostMessageLoop( ) throw( );  
  
```  
  
### Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
### Remarks  
 Override this method to perform custom application cleanup. The default implementation calls [CAtlExeModuleT::RevokeClassObjects](../vs140/CAtlExeModuleT--RevokeClassObjects.md).  
  
##  <a name="catlexemodulet__premessageloop"></a>  CAtlExeModuleT::PreMessageLoop  
 This method is called immediately before entering the message loop.  
  
```  
  
HRESULT PreMessageLoop(  
      int  nShowCmd  
   ) throw( );  
  
```  
  
### Parameters  
 `nShowCmd`  
 The value passed as the `nShowCmd` parameter in WinMain.  
  
### Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
### Remarks  
 Override this method to add custom initialization code for the application. The default implementation registers the class objects.  
  
##  <a name="catlexemodulet__registerclassobjects"></a>  CAtlExeModuleT::RegisterClassObjects  
 Registers the class object with OLE so other applications can connect to it.  
  
```  
  
HRESULT RegisterClassObjects(  
      DWORD  dwClsContext,  
      DWORD  dwFlags  
   ) throw( );  
  
```  
  
### Parameters  
 *dwClsContext*  
 Specifies the context in which the class object is to be run. Possible values are CLSCTX_INPROC_SERVER, CLSCTX_INPROC_HANDLER, or CLSCTX_LOCAL_SERVER.  
  
 `dwFlags`  
 Determines the connection types to the class object. Possible values are REGCLS_SINGLEUSE, REGCLS_MULTIPLEUSE, or REGCLS_MULTI_SEPARATE.  
  
### Return Value  
 Returns S_OK on success, S_FALSE if there were no classes to register, or an error HRESULT on failure.  
  
##  <a name="catlexemodulet__revokeclassobjects"></a>  CAtlExeModuleT::RevokeClassObjects  
 Removes the class object.  
  
```  
  
HRESULT RevokeClassObjects( ) throw( );  
  
```  
  
### Return Value  
 Returns S_OK on success, S_FALSE if there were no classes to register, or an error HRESULT on failure.  
  
##  <a name="catlexemodulet__run"></a>  CAtlExeModuleT::Run  
 This method executes code in the EXE module to initialize, run the message loop, and clean up.  
  
```  
  
HRESULT Run(  
      int  nShowCmd  
    = SW_HIDE   
   ) throw( );  
  
```  
  
### Parameters  
 `nShowCmd`  
 Specifies how the window is to be shown. This parameter can be one of the values discussed in the [WinMain](http://msdn.microsoft.com/library/windows/desktop/ms633559) section. Defaults to SW_HIDE.  
  
### Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
### Remarks  
 This method can be overridden. However, in practice is it better to override [CAtlExeModuleT::PreMessageLoop](../vs140/CAtlExeModuleT--PreMessageLoop.md), [CAtlExeModuleT::RunMessageLoop](../vs140/CAtlExeModuleT--RunMessageLoop.md), or [CAtlExeModuleT::PostMessageLoop](../vs140/CAtlExeModuleT--PostMessageLoop.md) instead.  
  
##  <a name="catlexemodulet__runmessageloop"></a>  CAtlExeModuleT::RunMessageLoop  
 This method executes the message loop.  
  
```  
  
void RunMessageLoop( ) throw( );  
  
```  
  
### Remarks  
 This method can be overridden to change the behavior of the message loop.  
  
##  <a name="catlexemodulet__uninitializecom"></a>  CAtlExeModuleT::UninitializeCom  
 Uninitializes COM.  
  
```  
  
static void UninitializeCom( ) throw( );  
  
```  
  
### Remarks  
 By default this method simply calls [CoUninitialize](http://msdn.microsoft.com/library/windows/desktop/ms688715) and is called from the destructor. Override this method if you override [CAtlExeModuleT::InitializeCom](../vs140/CAtlExeModuleT--InitializeCom.md).  
  
##  <a name="catlexemodulet__unlock"></a>  CAtlExeModuleT::Unlock  
 Decrements the module's lock count.  
  
```  
  
LONG Unlock( ) throw( );  
  
```  
  
### Return Value  
 Returns a value which may be useful for diagnostics or testing.  
  
##  <a name="catlexemodulet__winmain"></a>  CAtlExeModuleT::WinMain  
 This method implements the code required to run an EXE.  
  
```  
  
int WinMain(  
      int  nShowCmd  
   ) throw( );  
  
```  
  
### Parameters  
 `nShowCmd`  
 Specifies how the window is to be shown. This parameter can be one of the values discussed in the [WinMain](http://msdn.microsoft.com/library/windows/desktop/ms633559) section.  
  
### Return Value  
 Returns the executable's return value.  
  
### Remarks  
 This method can be overridden. If overriding [CAtlExeModuleT::PreMessageLoop](../vs140/CAtlExeModuleT--PreMessageLoop.md), [CAtlExeModuleT::PostMessageLoop](../vs140/CAtlExeModuleT--PostMessageLoop.md), or [CAtlExeModuleT::RunMessageLoop](../vs140/CAtlExeModuleT--RunMessageLoop.md) doesn't provide enough flexibility, it's possible to override the `WinMain` function using this method.  
  
## See Also  
 [ATLDuck Sample](../vs140/Visual-C---Samples.md)   
 [CAtlModuleT Class](../vs140/CAtlModuleT-Class.md)   
 [CAtlDllModuleT Class](../vs140/CAtlDllModuleT-Class.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)