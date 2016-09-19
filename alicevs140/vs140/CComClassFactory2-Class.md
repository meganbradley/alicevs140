---
title: "CComClassFactory2 Class"
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
ms.assetid: 19b66fd6-b9ed-47a0-822c-8132184f5a3e
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComClassFactory2 Class
This class implements the [IClassFactory2](http://msdn.microsoft.com/library/windows/desktop/ms692720) interface.  
  
## Syntax  
  
```  
  
template <class license>  
   class CComClassFactory2 : public IClassFactory2,  
      public CComObjectRootEx<CComGlobalsThreadModel>,  
      public  license  
  
```  
  
#### Parameters  
 *license*  
 A class that implements the following static functions:  
  
-   **static BOOL VerifyLicenseKey( BSTR**  `bstr`  **);**  
  
-   **static BOOL GetLicenseKey( DWORD**  `dwReserved` **, BSTR\***  `pBstr`  **);**  
  
-   **static BOOL IsLicenseValid( );**  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CComClassFactory2::CreateInstance](../vs140/CComClassFactory2--CreateInstance.md)|Creates an object of the specified CLSID.|  
|[CComClassFactory2::CreateInstanceLic](../vs140/CComClassFactory2--CreateInstanceLic.md)|Given a license key, creates an object of the specified CLSID.|  
|[CComClassFactory2::GetLicInfo](../vs140/CComClassFactory2--GetLicInfo.md)|Retrieves information describing the licensing capabilities of the class factory.|  
|[CComClassFactory2::LockServer](../vs140/CComClassFactory2--LockServer.md)|Locks the class factory in memory.|  
|[CComClassFactory2::RequestLicKey](../vs140/CComClassFactory2--RequestLicKey.md)|Creates and returns a license key.|  
  
## Remarks  
 `CComClassFactory2` implements the [IClassFactory2](http://msdn.microsoft.com/library/windows/desktop/ms692720) interface, which is an extension of [IClassFactory](http://msdn.microsoft.com/library/windows/desktop/ms694364).                 **IClassFactory2** controls object creation through a license. A class factory executing on a licensed machine can provide a run-time license key. This license key allows an application to instantiate objects when a full machine license does not exist.  
  
 ATL objects normally acquire a class factory by deriving from [CComCoClass](../vs140/CComCoClass-Class.md). This class includes the macro [DECLARE_CLASSFACTORY](../vs140/DECLARE_CLASSFACTORY.md), which declares [CComClassFactory](../vs140/CComClassFactory-Class.md) as the default class factory. To use `CComClassFactory2`, specify the [DECLARE_CLASSFACTORY2](../vs140/DECLARE_CLASSFACTORY2.md) macro in your object's class definition. For example:  
  
 [!CODE [NVC_ATL_COM#2](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#2)]  
  
 **CMyLicense**, the template parameter to `CComClassFactory2`, must implement the static functions `VerifyLicenseKey`, `GetLicenseKey`, and `IsLicenseValid`. The following is an example of a simple license class:  
  
 [!CODE [NVC_ATL_COM#3](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#3)]  
  
 `CComClassFactory2` derives from both **CComClassFactory2Base** and *license*.                 **CComClassFactory2Base**, in turn, derives from **IClassFactory2** and **CComObjectRootEx< CComGlobalsThreadModel >**.  
  
## Inheritance Hierarchy  
 `CComObjectRootBase`  
  
 `license`  
  
 [CComObjectRootEx](../vs140/CComObjectRootEx-Class.md)  
  
 `IClassFactory2`  
  
 `CComClassFactory2`  
  
## Requirements  
 **Header:** atlcom.h  
  
##  <a name="ccomclassfactory2__createinstance"></a>  CComClassFactory2::CreateInstance  
 Creates an object of the specified CLSID and retrieves an interface pointer to this object.  
  
```  
  
STDMETHOD(CreateInstance)(  
      LPUNKNOWN  pUnkOuter,  
      REFIID  riid,  
      void**  ppvObj  
   );  
  
```  
  
### Parameters  
 `pUnkOuter`  
 [in] If the object is being created as part of an aggregate, then `pUnkOuter` must be the outer unknown. Otherwise, `pUnkOuter` must be **NULL**.  
  
 `riid`  
 [in] The IID of the requested interface. If `pUnkOuter` is non-                                **NULL**, `riid` must be **IID_IUnknown**.  
  
 `ppvObj`  
 [out] A pointer to the interface pointer identified by `riid`. If the object does not support this interface, `ppvObj` is set to **NULL**.  
  
### Return Value  
 A standard `HRESULT` value.  
  
### Remarks  
 Requires the machine to be fully licensed. If a full machine license does not exist, call [CreateInstanceLic](../vs140/CComClassFactory2--CreateInstanceLic.md).  
  
##  <a name="ccomclassfactory2__createinstancelic"></a>  CComClassFactory2::CreateInstanceLic  
 Similar to [CreateInstance](../vs140/CComClassFactory2--CreateInstance.md), except that `CreateInstanceLic` requires a license key.  
  
```  
  
STDMETHOD(CreateInstanceLic)(  
      IUnknown*  pUnkOuter,  
      IUnknown* /*  pUnkReserved   
   */,  
      REFIID  riid,  
      BSTR  bstrKey,  
      void**  ppvObject  
   );  
  
```  
  
### Parameters  
 `pUnkOuter`  
 [in] If the object is being created as part of an aggregate, then `pUnkOuter` must be the outer unknown. Otherwise, `pUnkOuter` must be **NULL**.  
  
 *pUnkReserved*  
 [in] Not used. Must be **NULL**.  
  
 `riid`  
 [in] The IID of the requested interface. If `pUnkOuter` is non-                                **NULL**, `riid` must be **IID_IUnknown**.  
  
 `bstrKey`  
 [in] The run-time license key previously obtained from a call to `RequestLicKey`. This key is required to create the object.  
  
 `ppvObject`  
 [out] A pointer to the interface pointer specified by `riid`. If the object does not support this interface, `ppvObject` is set to **NULL**.  
  
### Return Value  
 A standard `HRESULT` value.  
  
### Remarks  
 You can obtain a license key using [RequestLicKey](../vs140/CComClassFactory2--RequestLicKey.md). In order to create an object on an unlicensed machine, you must call `CreateInstanceLic`.  
  
##  <a name="ccomclassfactory2__getlicinfo"></a>  CComClassFactory2::GetLicInfo  
 Fills a [LICINFO](http://msdn.microsoft.com/library/windows/desktop/ms690590) structure with information that describes the class factory's licensing capabilities.  
  
```  
  
STDMETHOD(GetLicInfo)(  
      LICINFO*  pLicInfo  
   );  
  
```  
  
### Parameters  
 *pLicInfo*  
 [out] Pointer to a **LICINFO** structure.  
  
### Return Value  
 A standard `HRESULT` value.  
  
### Remarks  
 The `fRuntimeKeyAvail` member of this structure indicates whether, given a license key, the class factory allows objects to be created on an unlicensed machine. The *fLicVerified* member indicates whether a full machine license exists.  
  
##  <a name="ccomclassfactory2__lockserver"></a>  CComClassFactory2::LockServer  
 Increments and decrements the module lock count by calling **_Module::Lock** and **_Module::Unlock**, respectively.  
  
```  
  
STDMETHOD(LockServer)(  
      BOOL  fLock  
   );  
  
```  
  
### Parameters  
 `fLock`  
 [in] If **TRUE**, the lock count is incremented; otherwise, the lock count is decremented.  
  
### Return Value  
 A standard `HRESULT` value.  
  
### Remarks  
 **_Module** refers to the global instance of [CComModule](../vs140/CComModule-Class.md) or a class derived from it.  
  
 Calling `LockServer` allows a client to hold onto a class factory so that multiple objects can be quickly created.  
  
##  <a name="ccomclassfactory2__requestlickey"></a>  CComClassFactory2::RequestLicKey  
 Creates and returns a license key, provided that the `fRuntimeKeyAvail` member of the [LICINFO](http://msdn.microsoft.com/library/windows/desktop/ms690590) structure is **TRUE**.  
  
```  
  
STDMETHOD(RequestLicKey)(  
      DWORD  dwReserved,  
      BSTR*  pbstrKey  
   );  
  
```  
  
### Parameters  
 `dwReserved`  
 [in] Not used. Must be zero.  
  
 `pbstrKey`  
 [out] Pointer to the license key.  
  
### Return Value  
 A standard `HRESULT` value.  
  
### Remarks  
 A license key is required for calling [CreateInstanceLic](../vs140/CComClassFactory2--CreateInstanceLic.md) to create an object on an unlicensed machine. If `fRuntimeKeyAvail` is **FALSE**, then objects can only be created on a fully licensed machine.  
  
 Call [GetLicInfo](../vs140/CComClassFactory2--GetLicInfo.md) to retrieve the value of `fRuntimeKeyAvail`.  
  
## See Also  
 [CComClassFactoryAutoThread Class](../vs140/CComClassFactoryAutoThread-Class.md)   
 [CComClassFactorySingleton Class](../vs140/CComClassFactorySingleton-Class.md)   
 [CComObjectRootEx Class](../vs140/CComObjectRootEx-Class.md)   
 [CComGlobalsThreadModel](../vs140/CComGlobalsThreadModel.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)