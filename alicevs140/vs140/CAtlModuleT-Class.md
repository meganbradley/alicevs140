---
title: "CAtlModuleT Class"
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
ms.assetid: 9b74d02f-9117-47b1-a05e-c5945f83dd2b
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlModuleT Class
This class implements an ATL module.  
  
## Syntax  
  
```  
  
template <class T  
   >   
   class ATL_NO_VTABLE CAtlModuleT :  
      public CAtlModule  
  
```  
  
#### Parameters  
 `T`  
 Your class derived from `CAtlModuleT`.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CAtlModuleT::CAtlModuleT](../vs140/CAtlModuleT--CAtlModuleT.md)|The constructor.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CAtlModuleT::InitLibId](../vs140/CAtlModuleT--InitLibId.md)|Initializes the data member containing the GUID of the current module.|  
|[CAtlModuleT::RegisterAppId](../vs140/CAtlModuleT--RegisterAppId.md)|Adds the EXE to the registry.|  
|[CAtlModuleT::RegisterServer](../vs140/CAtlModuleT--RegisterServer.md)|Adds the service to the registry.|  
|[CAtlModuleT::UnregisterAppId](../vs140/CAtlModuleT--UnregisterAppId.md)|Removes the EXE from the registry.|  
|[CAtlModuleT::UnregisterServer](../vs140/CAtlModuleT--UnregisterServer.md)|Removes the service from the registry.|  
|[CAtlModuleT::UpdateRegistryAppId](../vs140/CAtlModuleT--UpdateRegistryAppId.md)|Updates the EXE information in the registry.|  
  
## Remarks  
 `CAtlModuleT`, derived from [CAtlModule](../vs140/CAtlModule-Class.md), implements an Executable (EXE) or a Service (EXE) ATL module. An Executable module is a local, out-of-process server, whereas a Service module is a Windows application that runs in the background when Windows starts.  
  
 `CAtlModuleT` provides support for initializing, registering, and unregistering of the module.  
  
## Inheritance Hierarchy  
 [_ATL_MODULE](../vs140/_ATL_MODULE.md)  
  
 [CAtlModule](../vs140/CAtlModule-Class.md)  
  
 `CAtlModuleT`  
  
## Requirements  
 **Header:** atlbase.h  
  
##  <a name="catlmodulet__catlmodulet"></a>  CAtlModuleT::CAtlModuleT  
 The constructor.  
  
```  
  
CAtlModuleT( ) throw( );  
  
```  
  
### Remarks  
 Calls [CAtlModuleT::InitLibId](../vs140/CAtlModuleT--InitLibId.md).  
  
##  <a name="catlmodulet__initlibid"></a>  CAtlModuleT::InitLibId  
 Initializes the data member containing the GUID of the current module.  
  
```  
  
static void InitLibId( ) throw( );  
  
```  
  
### Remarks  
 Called by the constructor [CAtlModuleT::CAtlModuleT](../vs140/CAtlModuleT--CAtlModuleT.md).  
  
##  <a name="catlmodulet__registerappid"></a>  CAtlModuleT::RegisterAppId  
 Adds the EXE to the registry.  
  
```  
  
HRESULT RegisterAppId( ) throw( );  
  
```  
  
### Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
##  <a name="catlmodulet__registerserver"></a>  CAtlModuleT::RegisterServer  
 Adds the service to the registry.  
  
```  
  
HRESULT RegisterServer(  
      BOOL  bRegTypeLib  
    = FALSE,  
      const CLSID*  pCLSID  
    = NULL   
   ) throw( );  
  
```  
  
### Parameters  
 `bRegTypeLib`  
 TRUE if the type library is to be registered. The default value is FALSE.  
  
 `pCLSID`  
 Points to the CLSID of the object to be registered. If NULL (the default value), all objects in the object map will be registered.  
  
### Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
##  <a name="catlmodulet__unregisterappid"></a>  CAtlModuleT::UnregisterAppId  
 Removes the EXE from the registry.  
  
```  
  
HRESULT UnregisterAppId( ) throw( );  
  
```  
  
### Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
##  <a name="catlmodulet__unregisterserver"></a>  CAtlModuleT::UnregisterServer  
 Removes the service from the registry.  
  
```  
  
HRESULT UnregisterServer(  
      BOOL  bUnRegTypeLib,  
      const CLSID*  pCLSID  
    = NULL  
   ) throw( );  
  
```  
  
### Parameters  
 `bUnRegTypeLib`  
 TRUE if the type library is also to be unregistered.  
  
 `pCLSID`  
 Points to the CLSID of the object to be unregistered. If NULL (the default value), all objects in the object map will be unregistered.  
  
### Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
##  <a name="catlmodulet__updateregistryappid"></a>  CAtlModuleT::UpdateRegistryAppId  
 Updates the EXE information in the registry.  
  
```  
  
static HRESULT WINAPI UpdateRegistryAppId(  
      BOOL /* bRegister*/  
   ) throw( );  
  
```  
  
### Parameters  
 `bRegister`  
 Reserved.  
  
### Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## See Also  
 [CAtlModule Class](../vs140/CAtlModule-Class.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)   
 [Module Classes](../vs140/ATL-Module-Classes.md)