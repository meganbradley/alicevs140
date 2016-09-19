---
title: "CComClassFactorySingleton Class"
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
ms.assetid: debb983c-382b-487b-8d42-7ea26dc158b8
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComClassFactorySingleton Class
This class derives from [CComClassFactory](../vs140/CComClassFactory-Class.md) and uses [CComObjectGlobal](../vs140/CComObjectGlobal-Class.md) to construct a single object.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the Windows Runtime.  
  
## Syntax  
  
```  
  
template<  
   class  T>  
   class CComClassFactorySingleton :  
   public CComClassFactory  
  
```  
  
#### Parameters  
 `T`  
 Your class.  
  
 `CComClassFactorySingleton` derives from [CComClassFactory](../vs140/CComClassFactory-Class.md) and uses [CComObjectGlobal](../vs140/CComObjectGlobal-Class.md) to construct a single object. Each call to the `CreateInstance` method simply queries this object for an interface pointer.  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CComClassFactorySingleton::CreateInstance](../vs140/CComClassFactorySingleton--CreateInstance.md)|Queries `m_spObj` for an interface pointer.|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CComClassFactorySingleton::m_spObj](../vs140/CComClassFactorySingleton--m_spObj.md)|The [CComObjectGlobal](../vs140/CComObjectGlobal-Class.md) object constructed by `CComClassFactorySingleton`.|  
  
## Remarks  
 ATL objects normally acquire a class factory by deriving from [CComCoClass](../vs140/CComCoClass-Class.md). This class includes the macro [DECLARE_CLASSFACTORY](../vs140/DECLARE_CLASSFACTORY.md), which declares `CComClassFactory` as the default class factory. To use `CComClassFactorySingleton`, specify the [DECLARE_CLASSFACTORY_SINGLETON](../vs140/DECLARE_CLASSFACTORY_SINGLETON.md) macro in your object's class definition. For example:  
  
 [!CODE [NVC_ATL_COM#10](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#10)]  
  
## Inheritance Hierarchy  
 `CComObjectRootBase`  
  
 [CComObjectRootEx](../vs140/CComObjectRootEx-Class.md)  
  
 `IClassFactory`  
  
 [CComClassFactory](../vs140/CComClassFactory-Class.md)  
  
 `CComClassFactorySingleton`  
  
## Requirements  
 **Header:** atlcom.h  
  
##  <a name="ccomclassfactorysingleton__createinstance"></a>  CComClassFactorySingleton::CreateInstance  
 Calls `QueryInterface` through [m_spObj](../vs140/CComClassFactorySingleton--m_spObj.md) to retrieve an interface pointer.  
  
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
  
##  <a name="ccomclassfactorysingleton__m_spobj"></a>  CComClassFactorySingleton::m_spObj  
 The [CComObjectGlobal](../vs140/CComObjectGlobal-Class.md) object constructed by `CComClassFactorySingleton`.  
  
```  
  
CComPtr<IUnknown> m_spObj;  
  
```  
  
### Remarks  
 Each call to the [CreateInstance](../vs140/CComClassFactorySingleton--CreateInstance.md) method simply queries this object for an interface pointer.  
  
 Note that the current form of `m_spObj` presents a breaking change from the way that `CComClassFactorySingleton` worked in previous versions of ATL. In previous versions the `CComClassFactorySingleton` object was created at the same time as the class factory, during server initialization. In Visual C++.NET 2003, the object is created lazily, on the first request. This change could cause errors in programs that rely on early initialization.  
  
## See Also  
 [IClassFactory](http://msdn.microsoft.com/library/windows/desktop/ms694364)   
 [CComClassFactory2 Class](../vs140/CComClassFactory2-Class.md)   
 [CComClassFactoryAutoThread Class](../vs140/CComClassFactoryAutoThread-Class.md)   
 [CComObjectRootEx Class](../vs140/CComObjectRootEx-Class.md)   
 [CComGlobalsThreadModel](../vs140/CComGlobalsThreadModel.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)