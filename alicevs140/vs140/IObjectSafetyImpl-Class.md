---
title: "IObjectSafetyImpl Class"
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
ms.assetid: 64e32082-d910-4a8a-a5bf-ebed9145359d
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IObjectSafetyImpl Class
This class provides a default implementation of the `IObjectSafety` interface to allow a client to retrieve and set an object's safety levels.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
  
template <class  T  
   , DWORD  dwSupportedSafety>  
   class IObjectSafetyImpl  
  
```  
  
#### Parameters  
 `T`  
 Your class, derived from `IObjectSafetyImpl`.  
  
 *dwSupportedSafety*  
 Specifies the supported safety options for the control. Can be one of the following values:  
  
-   **INTERFACESAFE_FOR_UNTRUSTED_CALLER** The interface identified by the [SetInterfaceSafetyOptions](../vs140/IObjectSafetyImpl--SetInterfaceSafetyOptions.md) parameter `riid` should be made safe for scripting.  
  
-   **INTERFACESAFE_FOR_UNTRUSTED_DATA** The interface identified by the `SetInterfaceSafetyOptions` parameter `riid` should be made safe for untrusted data during initialization.  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[IObjectSafetyImpl::GetInterfaceSafetyOptions](../vs140/IObjectSafetyImpl--GetInterfaceSafetyOptions.md)|Retrieves the safety options supported by the object, as well as the safety options currently set for the object.|  
|[IObjectSafetyImpl::SetInterfaceSafetyOptions](../vs140/IObjectSafetyImpl--SetInterfaceSafetyOptions.md)|Makes the object safe for initialization or scripting.|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[IObjectSafetyImpl::m_dwCurrentSafety](../vs140/IObjectSafetyImpl--m_dwCurrentSafety.md)|Stores the object's current safety level.|  
  
## Remarks  
 Class `IObjectSafetyImpl` provides a default implementation of `IObjectSafety`. The `IObjectSafety` interface allows a client to retrieve and set an object's safety levels. For example, a web browser can call **IObjectSafety::SetInterfaceSafetyOptions** to make a control safe for initialization or safe for scripting.  
  
 Note that using the [IMPLEMENTED_CATEGORY](../vs140/IMPLEMENTED_CATEGORY.md) macro with the **CATID_SafeForScripting** and **CATID_SafeForInitializing** component categories provides an alternative way of specifying that a component is safe.  
  
 **Related Articles** [ATL Tutorial](../vs140/Active-Template-Library--ATL--Tutorial.md), [Creating an ATL Project](../vs140/Creating-an-ATL-Project.md)  
  
## Inheritance Hierarchy  
 `IObjectSafety`  
  
 `IObjectSafetyImpl`  
  
## Requirements  
 **Header:** atlctl.h  
  
##  <a name="iobjectsafetyimpl__getinterfacesafetyoptions"></a>  IObjectSafetyImpl::GetInterfaceSafetyOptions  
 Retrieves the safety options supported by the object, as well as the safety options currently set for the object.  
  
```  
  
HRESULT GetInterfaceSafetyOptions(  
      REFIID  riid,  
      DWORD*  pdwSupportedOptions,  
      DWORD*  pdwEnabledOptions  
   );  
  
```  
  
### Remarks  
 The implementation returns the appropriate values for any interface supported by the object's implementation of **IUnknown::QueryInterface**.  
  
> [!IMPORTANT]
>  Any object that supports `IObjectSafety` is responsible for its own security, and that of any object it delegates. The programmer must take into account issues arising from running code in the user's context, cross-site scripting and perform suitable zone checking.  
  
 See [IObjectSafety::GetInterfaceSafetyOptions](https://msdn.microsoft.com/en-us/library/aa768223.aspx) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
##  <a name="iobjectsafetyimpl__m_dwcurrentsafety"></a>  IObjectSafetyImpl::m_dwCurrentSafety  
 Stores the object's current safety level.  
  
```  
  
DWORD m_dwCurrentSafety;  
  
```  
  
##  <a name="iobjectsafetyimpl__setinterfacesafetyoptions"></a>  IObjectSafetyImpl::SetInterfaceSafetyOptions  
 Makes the object safe for initialization or scripting by setting the [m_dwCurrentSafety](../vs140/IObjectSafetyImpl--m_dwCurrentSafety.md) member to the appropriate value.  
  
```  
  
HRESULT SetInterfaceSafetyOptions(  
      REFIID  riid,  
      DWORD  dwOptionsSetMask,  
      DWORD  dwEnabledOptions  
   );  
  
```  
  
### Remarks  
 The implementation returns **E_NOINTERFACE** for any interface not supported by the object's implementation of **IUnknown::QueryInterface**.  
  
> [!IMPORTANT]
>  Any object that supports `IObjectSafety` is responsible for its own security, and that of any object it delegates. The programmer must take into account issues arising from running code in the user's context, cross-site scripting and perform suitable zone checking.  
  
 See [IObjectSafety::SetInterfaceSafetyOptions](https://msdn.microsoft.com/en-us/library/aa768225.aspx) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## See Also  
 [IObjectSafety Interface](https://msdn.microsoft.com/en-us/library/aa768224.aspx)   
 [Class Overview](../vs140/ATL-Class-Overview.md)