---
title: "CComClassFactoryAutoThread Class"
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
ms.assetid: 22008042-533f-4dd9-bf7e-191ee571f9a1
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComClassFactoryAutoThread Class
This class implements the [IClassFactory](http://msdn.microsoft.com/library/windows/desktop/ms694364) interface, and allows objects to be created in multiple apartments.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the Windows Runtime.  
  
## Syntax  
  
```  
  
class CComClassFactoryAutoThread : public IClassFactory,   
   public CComObjectRootEx< CComGlobalsThreadModel >  
  
```  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CComClassFactoryAutoThread::CreateInstance](../vs140/CComClassFactoryAutoThread--CreateInstance.md)|Creates an object of the specified CLSID.|  
|[CComClassFactoryAutoThread::LockServer](../vs140/CComClassFactoryAutoThread--LockServer.md)|Locks the class factory in memory.|  
  
## Remarks  
 `CComClassFactoryAutoThread` is similar to [CComClassFactory](../vs140/CComClassFactory-Class.md), but allows objects to be created in multiple apartments. To take advantage of this support, derive your EXE module from [CComAutoThreadModule](../vs140/CComAutoThreadModule-Class.md).  
  
 ATL objects normally acquire a class factory by deriving from [CComCoClass](../vs140/CComCoClass-Class.md). This class includes the macro [DECLARE_CLASSFACTORY](../vs140/DECLARE_CLASSFACTORY.md), which declares [CComClassFactory](../vs140/CComClassFactory-Class.md) as the default class factory. To use `CComClassFactoryAutoThread`, specify the [DECLARE_CLASSFACTORY_AUTO_THREAD](../vs140/DECLARE_CLASSFACTORY_AUTO_THREAD.md) macro in your object's class definition. For example:  
  
 [!CODE [NVC_ATL_COM#9](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#9)]  
  
## Inheritance Hierarchy  
 `CComObjectRootBase`  
  
 [CComObjectRootEx](../vs140/CComObjectRootEx-Class.md)  
  
 `IClassFactory`  
  
 `CComClassFactoryAutoThread`  
  
## Requirements  
 **Header:** atlcom.h  
  
##  <a name="ccomclassfactoryautothread__createinstance"></a>  CComClassFactoryAutoThread::CreateInstance  
 Creates an object of the specified CLSID and retrieves an interface pointer to this object.  
  
```  
  
STDMETHODIMP CreateInstance(  
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
 If your module derives from [CComAutoThreadModule](../vs140/CComAutoThreadModule-Class.md), `CreateInstance` first selects a thread to create the object in the associated apartment.  
  
##  <a name="ccomclassfactoryautothread__lockserver"></a>  CComClassFactoryAutoThread::LockServer  
 Increments and decrements the module lock count by calling **_Module::Lock** and **_Module::Unlock**, respectively.  
  
```  
  
STDMETHODIMP LockServer(  
      BOOL  fLock  
   );  
  
```  
  
### Parameters  
 `fLock`  
 [in] If **TRUE**, the lock count is incremented; otherwise, the lock count is decremented.  
  
### Return Value  
 A standard `HRESULT` value.  
  
### Remarks  
 When using `CComClassFactoryAutoThread`,                         **_Module** typically refers to the global instance of [CComAutoThreadModule](../vs140/CComAutoThreadModule-Class.md).  
  
 Calling `LockServer` allows a client to hold onto a class factory so that multiple objects can be quickly created.  
  
## See Also  
 [IClassFactory](http://msdn.microsoft.com/library/windows/desktop/ms694364)   
 [CComClassFactory2 Class](../vs140/CComClassFactory2-Class.md)   
 [CComClassFactorySingleton Class](../vs140/CComClassFactorySingleton-Class.md)   
 [CComObjectRootEx Class](../vs140/CComObjectRootEx-Class.md)   
 [CComGlobalsThreadModel](../vs140/CComGlobalsThreadModel.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)