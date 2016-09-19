---
title: "IDispEventImpl Class"
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
ms.assetid: a64b5288-35cb-4638-aad6-2d15b1c7cf7b
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDispEventImpl Class
This class provides implementations of the `IDispatch` methods.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
  
template <  
   UINT  nID,  
   class  T,  
   const IID*  pdiid  
   = &IID_NULL,  
   const GUID*  plibid  
   = &GUID_NULL,  
   WORD  wMajor  
   = 0,  
   WORD  wMinor  
   = 0,  
   class  tihclass  
   = CcomTypeInfoHolder>  
   class ATL_NO_VTABLE IDispEventImpl :  
   public IDispEventSimpleImpl< nID  
   ,  T  
   ,  pdiid>  
  
```  
  
#### Parameters  
 `nID`  
 A unique identifier for the source object. When `IDispEventImpl` is the base class for a composite control, use the resource ID of the desired contained control for this parameter. In other cases, use an arbitrary positive integer.  
  
 `T`  
 The user's class, which is derived from `IDispEventImpl`.  
  
 `pdiid`  
 The pointer to the IID of the event dispinterface implemented by this class. This interface must be defined in the type library denoted by `plibid`, `wMajor`, and `wMinor`.  
  
 `plibid`  
 A pointer to the type library that defines the dispatch interface pointed to by `pdiid`. If **&GUID_NULL**, the type library will be loaded from the object sourcing the events.  
  
 `wMajor`  
 The major version of the type library. The default value is 0.  
  
 `wMinor`  
 The minor version of the type library. The default value is 0.  
  
 `tihclass`  
 The class used to manage the type information for `T`. The default value is a class of type `CComTypeInfoHolder`; however, you can override this template parameter by providing a class of a type other than `CComTypeInfoHolder`.  
  
## Members  
  
### Public Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|[IDispEventImpl::_tihclass](../vs140/IDispEventImpl-Class.md)|The class used to manage the type information. By default, `CComTypeInfoHolder`.|  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[IDispEventImpl::IDispEventImpl](../vs140/IDispEventImpl--IDispEventImpl.md)|The constructor.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[IDispEventImpl::GetFuncInfoFromId](../vs140/IDispEventImpl--GetFuncInfoFromId.md)|Locates the function index for the specified dispatch identifier.|  
|[IDispEventImpl::GetIDsOfNames](../vs140/IDispEventImpl--GetIDsOfNames.md)|Maps a single member and an optional set of argument names to a corresponding set of integer DISPIDs.|  
|[IDispEventImpl::GetTypeInfo](../vs140/IDispEventImpl--GetTypeInfo.md)|Retrieves the type information for an object.|  
|[IDispEventImpl::GetTypeInfoCount](../vs140/IDispEventImpl--GetTypeInfoCount.md)|Retrieves the number of type information interfaces.|  
|[IDispEventImpl::GetUserDefinedType](../vs140/IDispEventImpl--GetUserDefinedType.md)|Retrieves the basic type of a user-defined type.|  
  
## Remarks  
 `IDispEventImpl` provides a way of implementing an event dispinterface without requiring you to supply implementation code for every method/event on that interface. `IDispEventImpl` provides implementations of the `IDispatch` methods. You only need to supply implementations for the events that you are interested in handling.  
  
 `IDispEventImpl` works in conjunction with the [event sink map](../vs140/BEGIN_SINK_MAP.md) in your class to route events to the appropriate handler function. To use this class:  
  
 Add a [SINK_ENTRY](../vs140/SINK_ENTRY.md) or [SINK_ENTRY_EX](../vs140/SINK_ENTRY_EX.md) macro to the event sink map for each event on each object that you want to handle. When using `IDispEventImpl` as a base class of a composite control, you can call [AtlAdviseSinkMap](../vs140/AtlAdviseSinkMap.md) to establish and break the connection with the event sources for all entries in the event sink map. In other cases, or for greater control, call [DispEventAdvise](../vs140/IDispEventSimpleImpl--DispEventAdvise.md) to establish the connection between the source object and the base class. Call [DispEventUnadvise](../vs140/IDispEventSimpleImpl--DispEventUnadvise.md) to break the connection.  
  
 You must derive from `IDispEventImpl` (using a unique value for `nID`) for each object for which you need to handle events. You can reuse the base class by unadvising against one source object then advising against a different source object, but the maximum number of source objects that can be handled by a single object at one time is limited by the number of `IDispEventImpl` base classes.  
  
 `IDispEventImpl` provides the same functionality as [IDispEventSimpleImpl](../vs140/IDispEventSimpleImpl-Class.md), except it gets type information about the interface from a type library rather than having it supplied as a pointer to an [_ATL_FUNC_INFO](../vs140/_ATL_FUNC_INFO-Structure.md) structure. Use `IDispEventSimpleImpl` when you do not have a type library describing the event interface or want to avoid the overhead associated with using the type library.  
  
> [!NOTE]
>  `IDispEventImpl` and `IDispEventSimpleImpl` provide their own implementation of **IUnknown::QueryInterface** enabling each `IDispEventImpl` and `IDispEventSimpleImpl` base class to act as a separate COM identity while still allowing direct access to class members in your main COM object.  
  
 CE ATL implementation of ActiveX event sinks only supports return values of type HRESULT or void from your event handler methods; any other return value is unsupported and its behavior is undefined.  
  
 For more information, see [Supporting IDispEventImpl](../vs140/Supporting-IDispEventImpl.md).  
  
## Inheritance Hierarchy  
 `_IDispEvent`  
  
 `_IDispEventLocator`  
  
 [IDispEventSimpleImpl](../vs140/IDispEventSimpleImpl-Class.md)  
  
 `IDispEventImpl`  
  
## Requirements  
 **Header:** atlcom.h  
  
##  <a name="idispeventimpl__getfuncinfofromid"></a>  IDispEventImpl::GetFuncInfoFromId  
 Locates the function index for the specified dispatch identifier.  
  
```  
  
HRESULT GetFuncInfoFromId(  
      const IID&  iid,  
      DISPID  dispidMember,  
      LCID  lcid,  
      _ATL_FUNC_INFO&  info  
   );  
  
```  
  
### Parameters  
 `iid`  
 [in] A reference to the ID of the function.  
  
 *dispidMember*  
 [in] The dispatch ID of the function.  
  
 `lcid`  
 [in] The locale context of the function ID.  
  
 `info`  
 [in] The structure indicating how the function is called.  
  
### Return Value  
 A standard `HRESULT` value.  
  
##  <a name="idispeventimpl__getidsofnames"></a>  IDispEventImpl::GetIDsOfNames  
 Maps a single member and an optional set of argument names to a corresponding set of integer DISPIDs, which can be used on subsequent calls to [IDispatch::Invoke](assetId:///964ade8e-9d8a-4d32-bd47-aa678912a54d).  
  
```  
  
STDMETHOD(GetIDsOfNames)(  
      REFIID  riid,  
      LPOLESTR*  rgszNames,  
      UINT  cNames,  
      LCID  lcid,  
      DISPID*  rgdispid  
   );  
  
```  
  
### Remarks  
 See [IDispatch::GetIDsOfNames](assetId:///6f6cf233-3481-436e-8d6a-51f93bf91619) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
##  <a name="idispeventimpl__gettypeinfo"></a>  IDispEventImpl::GetTypeInfo  
 Retrieves the type information for an object, which can then be used to get the type information for an interface.  
  
```  
  
STDMETHOD(GetTypeInfo)(  
      UINT  itinfo,  
      LCID  lcid,  
      ITypeInfo**  pptinfo  
   );  
  
```  
  
### Remarks  
  
##  <a name="idispeventimpl__gettypeinfocount"></a>  IDispEventImpl::GetTypeInfoCount  
 Retrieves the number of type information interfaces that an object provides (either 0 or 1).  
  
```  
  
STDMETHOD(GetTypeInfoCount)(  
      UINT*  pctinfo  
   );  
  
```  
  
### Remarks  
 See [IDispatch::GetTypeInfoCount](assetId:///da876d53-cb8a-465c-a43e-c0eb272e2a12) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
##  <a name="idispeventimpl__getuserdefinedtype"></a>  IDispEventImpl::GetUserDefinedType  
 Retrieves the basic type of a user-defined type.  
  
```  
  
VARTYPE GetUserDefinedType(  
      ITypeInfo * pTI,  
      HREFTYPE  hrt  
   );  
  
```  
  
### Parameters  
 `pTI`  
 [in] A pointer to the [ITypeInfo](assetId:///f3356463-3373-4279-bae1-953378aa2680) interface containing the user-defined type.  
  
 *hrt*  
 [in] A handle to the type description to be retrieved.  
  
### Return Value  
 The type of variant.  
  
### Remarks  
 See [ITypeInfo::GetRefTypeInfo](assetId:///61d3b31d-6591-4e55-9e82-5246a168be00).  
  
##  <a name="idispeventimpl__idispeventimpl"></a>  IDispEventImpl::IDispEventImpl  
 The constructor. Stores the values of the class template parameters `plibid`, `pdiid`, `wMajor`, and `wMinor`.  
  
```  
  
IDispEventImpl( );  
  
```  
  
##  <a name="idispeventimpl__tihclass"></a>  IDispEventImpl::tihclass  
 This typedef is an instance of the class template parameter `tihclass`.  
  
```  
  
typedef tihclass _tihclass;  
  
```  
  
### Remarks  
 By default, the class is `CComTypeInfoHolder`. `CComTypeInfoHolder` manages the type information for the class.  
  
## See Also  
 [_ATL_FUNC_INFO Structure](../vs140/_ATL_FUNC_INFO-Structure.md)   
 [IDispatchImpl Class](../vs140/IDispatchImpl-Class.md)   
 [IDispEventSimpleImpl Class](../vs140/IDispEventSimpleImpl-Class.md)   
 [SINK_ENTRY](../vs140/SINK_ENTRY.md)   
 [SINK_ENTRY_EX](../vs140/SINK_ENTRY_EX.md)   
 [SINK_ENTRY_INFO](../vs140/SINK_ENTRY_INFO.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)