---
title: "CComObject Class"
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
ms.assetid: e2b6433b-6349-4749-b4bc-acbd7a22c8b0
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComObject Class
This class implements **IUnknown** for a nonaggregated object.  
  
## Syntax  
  
```  
  
template<  
      class  Base>  
   class CComObject :  
      public  Base  
  
```  
  
#### Parameters  
 `Base`  
 Your class, derived from [CComObjectRoot](../vs140/CComObjectRoot-Class.md) or [CComObjectRootEx](../vs140/CComObjectRootEx-Class.md), as well as from any other interfaces you want to support on the object.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CComObject::CComObject](../vs140/CComObject--CComObject.md)|The constructor.|  
|[CComObject::~CComObject](../vs140/CComObject--~CComObject.md)|The destructor.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CComObject::AddRef](../vs140/CComObject--AddRef.md)|Increments the reference count on the object.|  
|[CComObject::CreateInstance](../vs140/CComObject--CreateInstance.md)|(Static) Creates a new `CComObject` object.|  
|[CComObject::QueryInterface](../vs140/CComObject--QueryInterface.md)|Retrieves a pointer to the requested interface.|  
|[CComObject::Release](../vs140/CComObject--Release.md)|Decrements the reference count on the object.|  
  
## Remarks  
 `CComObject` implements [IUnknown](http://msdn.microsoft.com/library/windows/desktop/ms680509) for a nonaggregated object. However, calls to `QueryInterface`, `AddRef`, and **Release** are delegated to `CComObjectRootEx`.  
  
 For more information about using `CComObject`, see the article [Fundamentals of ATL COM Objects](../vs140/Fundamentals-of-ATL-COM-Objects.md).  
  
## Inheritance Hierarchy  
 `Base`  
  
 `CComObject`  
  
## Requirements  
 **Header:** atlcom.h  
  
##  <a name="ccomobject__addref"></a>  CComObject::AddRef  
 Increments the reference count on the object.  
  
```  
  
STDMETHOD_(ULONG, AddRef)( );  
  
```  
  
### Return Value  
 This function returns the new incremented reference count on the object. This value may be useful for diagnostics or testing.  
  
##  <a name="ccomobject__ccomobject"></a>  CComObject::CComObject  
 The constructor increments the module lock count.  
  
```  
  
CComObject(  
      void* = NULL   
   );  
  
```  
  
### Parameters  
 **void\***  
 [in] This unnamed parameter is not used. It exists for symmetry with other **CCom***XXX*`Object`*XXX* constructors.  
  
### Remarks  
 The destructor decrements it.  
  
 If a `CComObject`-derived object is successfully constructed using the **new** operator, the initial reference count is 0. To set the reference count to the proper value (1), make a call to the [AddRef](../vs140/CComObject--AddRef.md) function.  
  
##  <a name="ccomobject___dtorccomobject"></a>  CComObject::~CComObject  
 The destructor.  
  
```  
  
CComObject( );  
  
```  
  
### Remarks  
 Frees all allocated resources, calls [FinalRelease](../vs140/CComObjectRootEx--FinalRelease.md), and decrements the module lock count.  
  
##  <a name="ccomobject__createinstance"></a>  CComObject::CreateInstance  
 This static function allows you to create a new **CComObject<**`Base`**>** object, without the overhead of [CoCreateInstance](http://msdn.microsoft.com/library/windows/desktop/ms686615).  
  
```  
  
static HRESULT WINAPI CreateInstance(  
      CComObject<  Base  
    >**  pp  
   );  
  
```  
  
### Parameters  
 `pp`  
 [out] A pointer to a **CComObject<**`Base`**>** pointer. If `CreateInstance` is unsuccessful, `pp` is set to **NULL**.  
  
### Return Value  
 A standard `HRESULT` value.  
  
### Remarks  
 The object returned has a reference count of zero, so call `AddRef` immediately, then use **Release** to free the reference on the object pointer when you're done.  
  
 If you do not need direct access to the object, but still want to create a new object without the overhead of `CoCreateInstance`, use [CComCoClass::CreateInstance](../vs140/CComCoClass--CreateInstance.md) instead.  
  
### Example  
 [!CODE [NVC_ATL_COM#38](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#38)]  
  
 [!CODE [NVC_ATL_COM#39](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#39)]  
  
##  <a name="ccomobject__queryinterface"></a>  CComObject::QueryInterface  
 Retrieves a pointer to the requested interface.  
  
```  
  
STDMETHOD(QueryInterface)(  
      REFIID  iid,  
      void**  ppvObject  
   );  
   template <class  Q>  
   HRESULT STDMETHODCALLTYPE QueryInterface(  
      Q**  pp  
   );  
  
```  
  
### Parameters  
 `iid`  
 [in] The identifier of the interface being requested.  
  
 `ppvObject`  
 [out] A pointer to the interface pointer identified by `iid`. If the object does not support this interface, `ppvObject` is set to **NULL**.  
  
 `pp`  
 [out] A pointer to the interface pointer identified by type `Q`. If the object does not support this interface, `pp` is set to **NULL**.  
  
### Return Value  
 A standard `HRESULT` value.  
  
##  <a name="ccomobject__release"></a>  CComObject::Release  
 Decrements the reference count on the object.  
  
```  
  
STDMETHOD_(ULONG, Release)( );  
  
```  
  
### Return Value  
 This function returns the new decremented reference count on the object. In debug builds, the return value may be useful for diagnostics or testing. In non-debug builds,                         **Release** always returns 0.  
  
## See Also  
 [CComAggObject Class](../vs140/CComAggObject-Class.md)   
 [CComPolyObject Class](../vs140/CComPolyObject-Class.md)   
 [DECLARE_AGGREGATABLE](../vs140/DECLARE_AGGREGATABLE.md)   
 [DECLARE_NOT_AGGREGATABLE](../vs140/DECLARE_NOT_AGGREGATABLE.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)