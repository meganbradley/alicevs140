---
title: "CComPolyObject Class"
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
ms.assetid: eaf67c18-e855-48ca-9b15-f1df3106121b
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComPolyObject Class
This class implements **IUnknown** for an aggregated or nonaggregated object.  
  
## Syntax  
  
```  
  
template<  
      class  contained>  
   class CComPolyObject : public IUnknown, public CComObjectRootEx  
      <  contained  
   ::_ThreadModel::ThreadModelNoCS >  
  
```  
  
#### Parameters  
 `contained`  
 Your class, derived from [CComObjectRoot](../vs140/CComObjectRoot-Class.md) or [CComObjectRootEx](../vs140/CComObjectRootEx-Class.md), as well as from any other interfaces you want to support on the object.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CComPolyObject::CComPolyObject](../vs140/CComPolyObject--CComPolyObject.md)|The constructor.|  
|[CComPolyObject::~CComPolyObject](../vs140/CComPolyObject--~CComPolyObject.md)|The destructor.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CComPolyObject::AddRef](../vs140/CComPolyObject--AddRef.md)|Increments the object's reference count.|  
|[CComPolyObject::CreateInstance](../vs140/CComPolyObject--CreateInstance.md)|(Static) Allows you to create a new **CComPolyObject<** `contained` **>** object without the overhead of [CoCreateInstance](http://msdn.microsoft.com/library/windows/desktop/ms686615).|  
|[CComPolyObject::FinalConstruct](../vs140/CComPolyObject--FinalConstruct.md)|Performs final initialization of `m_contained`.|  
|[CComPolyObject::FinalRelease](../vs140/CComPolyObject--FinalRelease.md)|Performs final destruction of `m_contained`.|  
|[CComPolyObject::QueryInterface](../vs140/CComPolyObject--QueryInterface.md)|Retrieves a pointer to the requested interface.|  
|[CComPolyObject::Release](../vs140/CComPolyObject--Release.md)|Decrements the object's reference count.|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CComPolyObject::m_contained](../vs140/CComPolyObject--m_contained.md)|Delegates **IUnknown** calls to the outer unknown if the object is aggregated or to the **IUnknown** of the object if the object is not aggregated.|  
  
## Remarks  
 `CComPolyObject` implements [IUnknown](http://msdn.microsoft.com/library/windows/desktop/ms680509) for an aggregated or nonaggregated object.  
  
 When an instance of `CComPolyObject` is created, the value of the outer unknown is checked. If it is **NULL**,                 **IUnknown** is implemented for a nonaggregated object. If the outer unknown is not **NULL**,                 **IUnknown** is implemented for an aggregated object.  
  
 The advantage of using `CComPolyObject` is that you avoid having both [CComAggObject](../vs140/CComAggObject-Class.md) and [CComObject](../vs140/CComObject-Class.md) in your module to handle the aggregated and nonaggregated cases. A single `CComPolyObject` object handles both cases. This means only one copy of the vtable and one copy of the functions exist in your module. If your vtable is large, this can substantially decrease your module size. However, if your vtable is small, using `CComPolyObject` can result in a slightly larger module size because it is not optimized for an aggregated or nonaggregated object, as are `CComAggObject` and `CComObject`.  
  
 If the `DECLARE_POLY_AGGREGATABLE` macro is specified in your object's class definition, `CComPolyObject` will be used to create your object. `DECLARE_POLY_AGGREGATABLE` will automatically be declared if you use the ATL Project Wizard to create a full control or Internet Explorer control.  
  
 If aggregated, the `CComPolyObject` object has its own **IUnknown**, separate from the outer object's **IUnknown**, and maintains its own reference count. `CComPolyObject` uses [CComContainedObject](../vs140/CComContainedObject-Class.md) to delegate to the outer unknown.  
  
 For more information about aggregation, see the article [Fundamentals of ATL COM Objects](../vs140/Fundamentals-of-ATL-COM-Objects.md).  
  
## Inheritance Hierarchy  
 `CComObjectRootBase`  
  
 [CComObjectRootEx](../vs140/CComObjectRootEx-Class.md)  
  
 `IUnknown`  
  
 `CComPolyObject`  
  
## Requirements  
 **Header:** atlcom.h  
  
##  <a name="ccompolyobject__addref"></a>  CComPolyObject::AddRef  
 Increments the reference count on the object.  
  
```  
  
STDMETHOD_(ULONG, AddRef)( );  
  
```  
  
### Return Value  
 A value that may be useful for diagnostics or testing.  
  
##  <a name="ccompolyobject__ccompolyobject"></a>  CComPolyObject::CComPolyObject  
 The constructor.  
  
```  
  
CComPolyObject(  
      void*  pv  
   );  
  
```  
  
### Parameters  
 `pv`  
 [in] A pointer to the outer unknown if the object is to be aggregated, or **NULL** if the object if the object is not aggregated.  
  
### Remarks  
 Initializes the `CComContainedObject` data member, [m_contained](../vs140/CComPolyObject--m_contained.md), and increments the module lock count.  
  
 The destructor decrements the module lock count.  
  
##  <a name="ccompolyobject___dtorccompolyobject"></a>  CComPolyObject::~CComPolyObject  
 The destructor.  
  
```  
  
~CComPolyObject( );  
  
```  
  
### Remarks  
 Frees all allocated resources, calls [FinalRelease](../vs140/CComPolyObject--FinalRelease.md), and decrements the module lock count.  
  
##  <a name="ccompolyobject__createinstance"></a>  CComPolyObject::CreateInstance  
 Allows you to create a new **CComPolyObject<**`contained` **>** object without the overhead of [CoCreateInstance](http://msdn.microsoft.com/library/windows/desktop/ms686615).  
  
```  
  
static HRESULT WINAPI CreateInstance(  
      LPUNKNOWN pUnkOuter,   
      CComPolyObject<  contained  
   >**  pp  
   );  
  
```  
  
### Parameters  
 `pp`  
 [out] A pointer to a **CComPolyObject<** `contained`**>** pointer. If `CreateInstance` is unsuccessful, `pp` is set to **NULL**.  
  
### Return Value  
 A standard `HRESULT` value.  
  
### Remarks  
 The object returned has a reference count of zero, so call `AddRef` immediately, then use **Release** to free the reference on the object pointer when you're done.  
  
 If you don't need direct access to the object, but still want to create a new object without the overhead of `CoCreateInstance`, use [CComCoClass::CreateInstance](../vs140/CComCoClass--CreateInstance.md) instead.  
  
##  <a name="ccompolyobject__finalconstruct"></a>  CComPolyObject::FinalConstruct  
 Called during the final stages of object construction, this method performs any final initialization on the [m_contained](../vs140/CComPolyObject--m_contained.md) data member.  
  
```  
  
HRESULT FinalConstruct( );  
  
```  
  
### Return Value  
 A standard `HRESULT` value.  
  
##  <a name="ccompolyobject__finalrelease"></a>  CComPolyObject::FinalRelease  
 Called during object destruction, this method frees the [m_contained](../vs140/CComPolyObject--m_contained.md) data member.  
  
```  
  
void FinalRelease( );  
  
```  
  
##  <a name="ccompolyobject__m_contained"></a>  CComPolyObject::m_contained  
 A [CComContainedObject](../vs140/CComContainedObject-Class.md) object derived from your class.  
  
```  
  
CComContainedObject<  contained  
    > m_contained;  
  
```  
  
### Parameters  
 `contained`  
 [in] Your class, derived from [CComObjectRoot](../vs140/CComObjectRoot-Class.md) or [CComObjectRootEx](../vs140/CComObjectRootEx-Class.md), as well as from any other interfaces you want to support on the object.  
  
### Remarks  
 **IUnknown** calls through `m_contained` are delegated to the outer unknown if the object is aggregated, or to the **IUnknown** of this object if the object is not aggregated.  
  
##  <a name="ccompolyobject__queryinterface"></a>  CComPolyObject::QueryInterface  
 Retrieves a pointer to the requested interface.  
  
```  
  
STDMETHOD(QueryInterface)(  
      REFIID  iid,  
      void**  ppvObject  
   );  
   template <class  Q>  
   HRESULT QueryInterface( Q  
    **  pp  
   );  
  
```  
  
### Parameters  
 `Q`  
 The COM interface.  
  
 `iid`  
 [in] The identifier of the interface being requested.  
  
 `ppvObject`  
 [out] A pointer to the interface pointer identified by `iid`. If the object does not support this interface, `ppvObject` is set to **NULL**.  
  
 `pp`  
 [out] A pointer to the interface identified by **__uuidof(Q)**.  
  
### Return Value  
 A standard `HRESULT` value.  
  
### Remarks  
 For an aggregated object, if the requested interface is **IUnknown**, `QueryInterface` returns a pointer to the aggregated object's own **IUnknown** and increments the reference count. Otherwise, this method queries for the interface through the `CComContainedObject` data member, [m_contained](../vs140/CComPolyObject--m_contained.md).  
  
##  <a name="ccompolyobject__release"></a>  CComPolyObject::Release  
 Decrements the reference count on the object.  
  
```  
  
STDMETHOD_(ULONG, Release)( );  
  
```  
  
### Return Value  
 In debug builds,                         **Release** returns a value that may be useful for diagnostics or testing. In nondebug builds,                         **Release** always returns 0.  
  
## See Also  
 [CComObjectRootEx Class](../vs140/CComObjectRootEx-Class.md)   
 [DECLARE_POLY_AGGREGATABLE](../vs140/DECLARE_POLY_AGGREGATABLE.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)