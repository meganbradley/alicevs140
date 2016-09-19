---
title: "CComModule Class"
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
ms.assetid: f5face2c-8fd8-40e6-9ec3-54ab74701769
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComModule Class
As of ATL 7.0, `CComModule` is deprecated: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the Windows Runtime.  
  
## Syntax  
  
```  
class CComModule : public _ATL_MODULE  
```  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CComModule::GetClassObject](../vs140/CComModule--GetClassObject.md)|Creates an object of a specified CLSID. For DLLs only.|  
|[CComModule::GetModuleInstance](../vs140/CComModule--GetModuleInstance.md)|Returns `m_hInst`.|  
|[CComModule::GetResourceInstance](../vs140/CComModule--GetResourceInstance.md)|Returns `m_hInstResource`.|  
|[CComModule::GetTypeLibInstance](../vs140/CComModule--GetTypeLibInstance.md)|Returns `m_hInstTypeLib`.|  
|[CComModule::Init](../vs140/CComModule--Init.md)|Initializes data members.|  
|[CComModule::RegisterClassHelper](../vs140/CComModule--RegisterClassHelper.md)|Enters an object's standard class registration in the system registry.|  
|[CComModule::RegisterClassObjects](../vs140/CComModule--RegisterClassObjects.md)|Registers the class object. For EXEs only.|  
|[CComModule::RegisterServer](../vs140/CComModule--RegisterServer.md)|Updates the system registry for each object in the object map.|  
|[CComModule::RegisterTypeLib](../vs140/CComModule--RegisterTypeLib.md)|Registers a type library.|  
|[CComModule::RevokeClassObjects](../vs140/CComModule--RevokeClassObjects.md)|Revokes the class object. For EXEs only.|  
|[CComModule::Term](../vs140/CComModule--Term.md)|Releases data members.|  
|[CComModule::UnregisterClassHelper](../vs140/CComModule--UnregisterClassHelper.md)|Removes an object's standard class registration from the system registry.|  
|[CComModule::UnregisterServer](../vs140/CComModule--UnregisterServer.md)|Unregisters each object in the object map.|  
|[CComModule::UpdateRegistryClass](../vs140/CComModule--UpdateRegistryClass.md)|Registers or unregisters an object's standard class registration.|  
|[CComModule::UpdateRegistryFromResourceD](../vs140/CComModule--UpdateRegistryFromResourceD.md)|Runs the script contained in a specified resource to register or unregister an object.|  
|[CComModule::UpdateRegistryFromResourceS](../vs140/CComModule--UpdateRegistryFromResourceS.md)|Statically links to the ATL Registry Component. Runs the script contained in a specified resource to register or unregister an object.|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CComModule::m_csObjMap](../vs140/CComModule--m_csObjMap.md)|Ensures synchronized access to the object map information.|  
|[CComModule::m_csTypeInfoHolder](../vs140/CComModule--m_csTypeInfoHolder.md)|Ensures synchronized access to the type library information.|  
|[CComModule::m_csWindowCreate](../vs140/CComModule--m_csWindowCreate.md)|Ensures synchronized access to window class information and static data used during window creation.|  
|[CComModule::m_hInst](../vs140/CComModule--m_hInst.md)|Contains the handle to the module instance.|  
|[CComModule::m_hInstResource](../vs140/CComModule--m_hInstResource.md)|By default, contains the handle to the module instance.|  
|[CComModule::m_hInstTypeLib](../vs140/CComModule--m_hInstTypeLib.md)|By default, contains the handle to the module instance.|  
|[CComModule::m_pObjMap](../vs140/CComModule--m_pObjMap.md)|Points to the object map maintained by the module instance.|  
  
## Remarks  
  
> [!NOTE]
>  This class is deprecated, and the ATL code generation wizards now use the [CAtlAutoThreadModule](../vs140/CAtlAutoThreadModule-Class.md) and [CAtlModule](../vs140/CAtlModule-Class.md) derived classes. See [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more information. The information that follows is for use with applications created with older releases of ATL. `CComModule` is still part of ATL for backwards capability.  
  
 `CComModule` implements a COM server module, allowing a client to access the module's components. `CComModule` supports both DLL (in-process) and EXE (local) modules.  
  
 A `CComModule` instance uses an object map to maintain a set of class object definitions. This object map is implemented as an array of `_ATL_OBJMAP_ENTRY` structures, and contains information for:  
  
-   Entering and removing object descriptions in the system registry.  
  
-   Instantiating objects through a class factory.  
  
-   Establishing communication between a client and the root object in the component.  
  
-   Performing lifetime management of class objects.  
  
 When you run the ATL COM AppWizard, the wizard automatically generates `_Module`, a global instance of `CComModule` or a class derived from it. For more information about the ATL Project Wizard, see the article [Creating an ATL Project](../vs140/Creating-an-ATL-Project.md).  
  
 In addition to `CComModule`, ATL provides [CComAutoThreadModule](../vs140/CComAutoThreadModule-Class.md), which implements an apartment-model module for EXEs and Windows services. Derive your module from `CComAutoThreadModule` when you want to create objects in multiple apartments.  
  
## Inheritance Hierarchy  
 [_ATL_MODULE](../vs140/_ATL_MODULE.md)  
  
 [CAtlModule](../vs140/CAtlModule-Class.md)  
  
 [CAtlModuleT](../vs140/CAtlModuleT-Class.md)  
  
 `CComModule`  
  
## Requirements  
 `Header:` atlbase.h  
  
##  <a name="ccommodule__getclassobject"></a>  CComModule::GetClassObject  
 As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
```  
  
HRESULT GetClassObject(  
      REFCLSID  rclsid,  
      REFIID  riid,  
      LPVOID*  ppv  
   ) throw( );  
  
```  
  
### Parameters  
 `rclsid`  
 [in] The CLSID of the object to be created.  
  
 `riid`  
 [in] The IID of the requested interface.  
  
 `ppv`  
 [out] A pointer to the interface pointer identified by `riid`. If the object does not support this interface, `ppv` is set to **NULL**.  
  
### Return Value  
 A standard HRESULT value.  
  
### Remarks  
 Creates an object of the specified CLSID and retrieves an interface pointer to this object.  
  
 `GetClassObject` is only available to DLLs.  
  
##  <a name="ccommodule__getmoduleinstance"></a>  CComModule::GetModuleInstance  
 As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
```  
  
HINSTANCE GetModuleInstance( ) throw( );  
  
```  
  
### Return Value  
 The `HINSTANCE` identifying this module.  
  
### Remarks  
 Returns the [m_hInst](../vs140/CComModule--m_hInst.md) data member.  
  
##  <a name="ccommodule__getresourceinstance"></a>  CComModule::GetResourceInstance  
 As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
```  
  
HINSTANCE GetResourceInstance( ) throw( );  
  
```  
  
### Return Value  
 An `HINSTANCE`.  
  
### Remarks  
 Returns the [m_hInstResource](../vs140/CComModule--m_hInstResource.md) data member.  
  
##  <a name="ccommodule__gettypelibinstance"></a>  CComModule::GetTypeLibInstance  
 As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
```  
  
HINSTANCE GetTypeLibInstance( ) const throw( );  
  
```  
  
### Return Value  
 An `HINSTANCE`.  
  
### Remarks  
 Returns the [m_hInstTypeLib](../vs140/CComModule--m_hInstTypeLib.md) data member.  
  
##  <a name="ccommodule__init"></a>  CComModule::Init  
 As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
```  
  
HRESULT Init(  
      _ATL_OBJMAP_ENTRY*  p,  
      HINSTANCE  h,  
      const GUID*  plibid  
    = NULL  
   ) throw( );  
  
```  
  
### Parameters  
 `p`  
 [in] A pointer to an array of object map entries.  
  
 `h`  
 [in] The `HINSTANCE` passed to **DLLMain** or `WinMain`.  
  
 `plibid`  
 [in] A pointer to the LIBID of the type library associated with the project.  
  
### Return Value  
 A standard HRESULT value.  
  
### Remarks  
 Initializes all data members.  
  
##  <a name="ccommodule__m_csobjmap"></a>  CComModule::m_csObjMap  
 As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
```  
  
CRITICAL_SECTION m_csObjMap;  
  
```  
  
### Remarks  
 Ensures synchronized access to the object map.  
  
##  <a name="ccommodule__m_cstypeinfoholder"></a>  CComModule::m_csTypeInfoHolder  
 As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
```  
  
CRITICAL_SECTION m_csTypeInfoHolder;  
  
```  
  
### Remarks  
 Ensures synchronized access to the type library.  
  
##  <a name="ccommodule__m_cswindowcreate"></a>  CComModule::m_csWindowCreate  
 As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
```  
  
CRITICAL_SECTION m_csWindowCreate;  
  
```  
  
### Remarks  
 Ensures synchronized access to window class information and to static data used during window creation.  
  
##  <a name="ccommodule__m_hinst"></a>  CComModule::m_hInst  
 As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
```  
  
HINSTANCE m_hInst;  
  
```  
  
### Remarks  
 Contains the handle to the module instance.  
  
 The [Init](../vs140/CComModule--Init.md) method sets `m_hInst` to the handle passed to **DLLMain** or `WinMain`.  
  
##  <a name="ccommodule__m_hinstresource"></a>  CComModule::m_hInstResource  
 As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
```  
  
HINSTANCE m_hInstResource;  
  
```  
  
### Remarks  
 By default, contains the handle to the module instance.  
  
 The [Init](../vs140/CComModule--Init.md) method sets `m_hInstResource` to the handle passed to **DLLMain** or `WinMain`. You can explicitly set `m_hInstResource` to the handle to a resource.  
  
 The [GetResourceInstance](../vs140/CComModule--GetResourceInstance.md) method returns the handle stored in `m_hInstResource`.  
  
##  <a name="ccommodule__m_hinsttypelib"></a>  CComModule::m_hInstTypeLib  
 As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
```  
  
HINSTANCE m_hInstTypeLib;  
  
```  
  
### Remarks  
 By default, contains the handle to the module instance.  
  
 The [Init](../vs140/CComModule--Init.md) method sets `m_hInstTypeLib` to the handle passed to **DLLMain** or `WinMain`. You can explicitly set `m_hInstTypeLib` to the handle to a type library.  
  
 The [GetTypeLibInstance](../vs140/CComModule--GetTypeLibInstance.md) method returns the handle stored in `m_hInstTypeLib`.  
  
##  <a name="ccommodule__m_pobjmap"></a>  CComModule::m_pObjMap  
 As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
```  
  
_ATL_OBJMAP_ENTRY* m_pObjMap;  
  
```  
  
### Remarks  
 Points to the object map maintained by the module instance.  
  
##  <a name="ccommodule__registerclasshelper"></a>  CComModule::RegisterClassHelper  
 As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
```  
  
ATL_DEPRECATED HRESULT RegisterClassHelper(  
      const CLSID&  clsid,  
      LPCTSTR  lpszProgID,  
      LPCTSTR  lpszVerIndProgID,  
      UINT  nDescID,  
      DWORD  dwFlags  
   );  
  
```  
  
### Parameters  
 `clsid`  
 [in] The CLSID of the object to be registered.  
  
 `lpszProgID`  
 [in] The ProgID associated with the object.  
  
 `lpszVerIndProgID`  
 [in] The version-independent ProgID associated with the object.  
  
 `nDescID`  
 [in] The identifier of a string resource for the object's description.  
  
 `dwFlags`  
 [in] Specifies the threading model to enter in the registry. Possible values are **THREADFLAGS_APARTMENT**,                                 **THREADFLAGS_BOTH**, or **AUTPRXFLAG**.  
  
### Return Value  
 A standard HRESULT value.  
  
### Remarks  
 Enters an object's standard class registration in the system registry.  
  
 The [UpdateRegistryClass](../vs140/CComModule--UpdateRegistryClass.md) method calls `RegisterClassHelper`.  
  
##  <a name="ccommodule__registerclassobjects"></a>  CComModule::RegisterClassObjects  
 As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
```  
  
HRESULT RegisterClassObjects(  
      DWORD  dwClsContext,  
      DWORD  dwFlags  
   ) throw( );  
  
```  
  
### Parameters  
 `dwClsContext`  
 [in] Specifies the context in which the class object is to be run. Possible values are **CLSCTX_INPROC_SERVER**,                                 **CLSCTX_INPROC_HANDLER**, or **CLSCTX_LOCAL_SERVER**. For a description of these values, see [CLSCTX](http://msdn.microsoft.com/library/windows/desktop/ms693716) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `dwFlags`  
 [in] Determines the connection types to the class object. Possible values are **REGCLS_SINGLEUSE**,                                 **REGCLS_MULTIPLEUSE**, or **REGCLS_MULTI_SEPARATE**. For a description of these values, see [REGCLS](http://msdn.microsoft.com/library/windows/desktop/ms679697) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
### Return Value  
 A standard HRESULT value.  
  
### Remarks  
 Registers an EXE class object with OLE so other applications can connect to it. This method                        is only available to EXEs.  
  
##  <a name="ccommodule__registerserver"></a>  CComModule::RegisterServer  
 As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
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
 [in] Indicates whether the type library will be registered. The default value is **FALSE**.  
  
 `pCLSID`  
 [in] Points to the CLSID of the object to be registered. If **NULL** (the default value), all objects in the object map will be registered.  
  
### Return Value  
 A standard HRESULT value.  
  
### Remarks  
 Depending on the `pCLSID` parameter, updates the system registry for a single class object or for all objects in the object map.  
  
 If `bRegTypeLib` is **TRUE**, the type library information will also be updated.  
  
 See [OBJECT_ENTRY_AUTO](../vs140/OBJECT_ENTRY_AUTO.md) for information on how to add an entry to the object map.  
  
 `RegisterServer` will be called automatically by **DLLRegisterServer** for a DLL or by `WinMain` for an EXE run with the **/RegServer** command line option.  
  
##  <a name="ccommodule__registertypelib"></a>  CComModule::RegisterTypeLib  
 As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
```  
  
HRESULT RegisterTypeLib( ) throw( );   
   HRESULT RegisterTypeLib(  
      LPCTSTR  lpszIndex  
   ) throw( );  
  
```  
  
### Parameters  
 `lpszIndex`  
 [in] String in the format `"\\N"`, where `N` is the integer index of the TYPELIB resource.  
  
### Return Value  
 A standard HRESULT value.  
  
### Remarks  
 Adds information about a type library to the system registry.  
  
 If the module instance contains multiple type libraries, use the second version of this method to specify which type library should be used.  
  
##  <a name="ccommodule__revokeclassobjects"></a>  CComModule::RevokeClassObjects  
 As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
```  
  
HRESULT RevokeClassObjects( ) throw( );  
  
```  
  
### Return Value  
 A standard HRESULT value.  
  
### Remarks  
 Removes the class object. This method                        is only available to EXEs.  
  
##  <a name="ccommodule__term"></a>  CComModule::Term  
 As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
```  
  
void Term( ) throw( );  
  
```  
  
### Remarks  
 Releases all data members.  
  
##  <a name="ccommodule__unregisterclasshelper"></a>  CComModule::UnregisterClassHelper  
 As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
```  
  
ATL_DEPRECATED HRESULT UnregisterClassHelper(  
      const CLSID&  clsid,  
      LPCTSTR  lpszProgID,  
      LPCTSTR  lpszVerIndProgID  
   );  
  
```  
  
### Parameters  
 `clsid`  
 [in] The CLSID of the object to be unregistered.  
  
 `lpszProgID`  
 [in] The ProgID associated with the object.  
  
 `lpszVerIndProgID`  
 [in] The version-independent ProgID associated with the object.  
  
### Return Value  
 A standard HRESULT value.  
  
### Remarks  
 Removes an object's standard class registration from the system registry.  
  
 The [UpdateRegistryClass](../vs140/CComModule--UpdateRegistryClass.md) method calls `UnregisterClassHelper`.  
  
##  <a name="ccommodule__unregisterserver"></a>  CComModule::UnregisterServer  
 As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
```  
  
HRESULT UnregisterServer(  
      const CLSID*  pCLSID  
    = NULL  
   ) throw ( );  
   inline HRESULT UnregisterServer(  
      BOOL  bUnRegTypeLib,  
      const CLSID*  pCLSID   
   = NULL  
   ) throw ( );  
  
```  
  
### Parameters  
 `bUnRegTypeLib`  
 If **TRUE**, the type library is also unregistered.  
  
 `pCLSID`  
 Points to the CLSID of the object to be unregistered. If **NULL** (the default value), all objects in the object map will be unregistered.  
  
### Return Value  
 A standard HRESULT value.  
  
### Remarks  
 Depending on the `pCLSID` parameter, unregisters either a single class object or all objects in the object map.  
  
 `UnregisterServer` will be called automatically by **DLLUnregisterServer** for a DLL or by `WinMain` for an EXE run with the **/UnregServer** command line option.  
  
 See [OBJECT_ENTRY_AUTO](../vs140/OBJECT_ENTRY_AUTO.md) for information on how to add an entry to the object map.  
  
##  <a name="ccommodule__updateregistryclass"></a>  CComModule::UpdateRegistryClass  
 As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
```  
  
ATL_DEPRECATED HRESULT UpdateRegistryClass(  
      const CLSID&  clsid,  
      LPCTSTR  lpszProgID,  
      LPCTSTR  lpszVerIndProgID,  
      UINT  nDescID,  
      DWORD  dwFlags,  
      BOOL  bRegister  
   );  
   ATL_DEPRECATED HRESULT UpdateRegistryClass(  
      const CLSID&  clsid,  
      LPCTSTR  lpszProgID,  
      LPCTSTR  lpszVerIndProgID,  
      LPCTSTR  szDesc,  
      DWORD  dwFlags,  
      BOOL  bRegister  
   );  
  
```  
  
### Parameters  
 `clsid`  
 The CLSID of the object to be registered or unregistered.  
  
 `lpszProgID`  
 The ProgID associated with the object.  
  
 `lpszVerIndProgID`  
 The version-independent ProgID associated with the object.  
  
 `nDescID`  
 The identifier of the string resource for the object's description.  
  
 `szDesc`  
 A string containing the object's description.  
  
 `dwFlags`  
 Specifies the threading model to enter in the registry. Possible values are **THREADFLAGS_APARTMENT**,                                 **THREADFLAGS_BOTH**, or **AUTPRXFLAG**.  
  
 `bRegister`  
 Indicates whether the object should be registered.  
  
### Return Value  
 A standard HRESULT value.  
  
### Remarks  
 If `bRegister` is **TRUE**, this method enters the object's standard class registration in the system registry.  
  
 If `bRegister` is **FALSE**, it removes the object's registration.  
  
 Depending on the value of `bRegister`, `UpdateRegistryClass` calls either [RegisterClassHelper](../vs140/CComModule--RegisterClassHelper.md) or [UnregisterClassHelper](../vs140/CComModule--UnregisterClassHelper.md).  
  
 By specifying the [DECLARE_REGISTRY](../vs140/DECLARE_REGISTRY.md) macro, `UpdateRegistryClass` will be invoked automatically when your object map is processed.  
  
##  <a name="ccommodule__updateregistryfromresourced"></a>  CComModule::UpdateRegistryFromResourceD  
 As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
```  
  
virtual HRESULT UpdateRegistryFromResourceD(  
      LPCTSTR  lpszRes,  
      BOOL  bRegister,  
      struct _ATL_REGMAP_ENTRY*  pMapEntries  
    = NULL   
   ) throw( );  
   virtual HRESULT UpdateRegistryFromResourceD(  
      UINT  nResID,  
      BOOL  bRegister,  
      struct _ATL_REGMAP_ENTRY*  pMapEntries  
    = NULL   
   ) throw ( );  
  
```  
  
### Parameters  
 `lpszRes`  
 [in] A resource name.  
  
 `nResID`  
 [in] A resource ID.  
  
 `bRegister`  
 [in] Indicates whether the object should be registered.  
  
 `pMapEntries`  
 [in] A pointer to the replacement map storing values associated with the script's replaceable parameters. ATL automatically uses `%MODULE%`. To use additional replaceable parameters, see the Remarks for details. Otherwise, use the **NULL** default value.  
  
### Return Value  
 A standard HRESULT value.  
  
### Remarks  
 Runs the script contained in the resource specified by `lpszRes` or `nResID`.  
  
 If `bRegister` is **TRUE**, this method registers the object in the system registry; otherwise, it unregisters the object.  
  
 By specifying the [DECLARE_REGISTRY_RESOURCE](../vs140/DECLARE_REGISTRY_RESOURCE.md) or [DECLARE_REGISTRY_RESOURCEID](../vs140/DECLARE_REGISTRY_RESOURCEID.md) macro, `UpdateRegistryFromResourceD` will be invoked automatically when your object map is processed.  
  
> [!NOTE]
>  To substitute replacement values at run time, do not specify the `DECLARE_REGISTRY_RESOURCE` or `DECLARE_REGISTRY_RESOURCEID` macro. Instead, create an array of **_ATL_REGMAP_ENTRIES** structures, where each entry contains a variable placeholder paired with a value to replace the placeholder at run time. Then call `UpdateRegistryFromResourceD`, passing the array for the `pMapEntries` parameter. This adds all the replacement values in the **_ATL_REGMAP_ENTRIES** structures to the Registrar's replacement map.  
  
> [!NOTE]
>  To statically link to the ATL Registry Component (Registrar), see [UpdateRegistryFromResourceS](../vs140/CComModule--UpdateRegistryFromResourceS.md).  
  
 For more information about replaceable parameters and scripting, see the article [The ATL Registry Component (Registrar)](../vs140/ATL-Registry-Component--Registrar-.md).  
  
##  <a name="ccommodule__updateregistryfromresources"></a>  CComModule::UpdateRegistryFromResourceS  
 As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
```  
  
virtual HRESULT UpdateRegistryFromResourceS(  
      LPCTSTR  lpszRes,  
      BOOL  bRegister,  
      struct _ATL_REGMAP_ENTRY*  pMapEntries  
    = NULL   
   ) throw( );  
   virtual HRESULT UpdateRegistryFromResourceS(  
      UINT  nResID,  
      BOOL  bRegister,  
      struct _ATL_REGMAP_ENTRY*  pMapEntries  
    = NULL   
   ) throw( );  
  
```  
  
### Parameters  
 `lpszRes`  
 [in] A resource name.  
  
 `nResID`  
 [in] A resource ID.  
  
 `bRegister`  
 [in] Indicates whether the resource script should be registered.  
  
 `pMapEntries`  
 [in] A pointer to the replacement map storing values associated with the script's replaceable parameters. ATL automatically uses `%MODULE%`. To use additional replaceable parameters, see the Remarks for details. Otherwise, use the **NULL** default value.  
  
### Return Value  
 A standard HRESULT value.  
  
### Remarks  
 Similar to [UpdateRegistryFromResourceD](../vs140/CComModule--UpdateRegistryFromResourceD.md) except `UpdateRegistryFromResourceS` creates a static link to the ATL Registry Component (Registrar).  
  
 `UpdateRegistryFromResourceS` will be invoked automatically when your object map is processed, provided you add `#define _ATL_STATIC_REGISTRY` to your stdafx.h.  
  
> [!NOTE]
>  To substitute replacement values at run time, do not specify the [DECLARE_REGISTRY_RESOURCE](../vs140/DECLARE_REGISTRY_RESOURCE.md) or [DECLARE_REGISTRY_RESOURCEID](../vs140/DECLARE_REGISTRY_RESOURCEID.md) macro. Instead, create an array of **_ATL_REGMAP_ENTRIES** structures, where each entry contains a variable placeholder paired with a value to replace the placeholder at run time. Then call `UpdateRegistryFromResourceS`, passing the array for the `pMapEntries` parameter. This adds all the replacement values in the **_ATL_REGMAP_ENTRIES** structures to the Registrar's replacement map.  
  
 For more information about replaceable parameters and scripting, see the article [The ATL Registry Component (Registrar)](../vs140/ATL-Registry-Component--Registrar-.md).  
  
## See Also  
 [Class Overview](../vs140/ATL-Class-Overview.md)