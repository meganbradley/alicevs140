---
title: "CComObjectGlobal Class"
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
ms.assetid: 79bdee55-66e4-4536-b5b3-bdf09f78b9a6
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComObjectGlobal Class
This class manages a reference count on the module containing your `Base` object.  
  
## Syntax  
  
```  
  
template<  
      class  Base>  
   class  
   CComObjectGlobal  
   :  
   public Base  
  
```  
  
#### Parameters  
 `Base`  
 Your class, derived from [CComObjectRoot](../vs140/CComObjectRoot-Class.md) or [CComObjectRootEx](../vs140/CComObjectRootEx-Class.md), as well as from any other interface you want to support on the object.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CComObjectGlobal::CComObjectGlobal](../vs140/CComObjectGlobal--CComObjectGlobal.md)|The constructor.|  
|[CComObjectGlobal::~CComObjectGlobal](../vs140/CComObjectGlobal--~CComObjectGlobal.md)|The destructor.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CComObjectGlobal::AddRef](../vs140/CComObjectGlobal--AddRef.md)|Implements a global `AddRef`.|  
|[CComObjectGlobal::QueryInterface](../vs140/CComObjectGlobal--QueryInterface.md)|Implements a global `QueryInterface`.|  
|[CComObjectGlobal::Release](../vs140/CComObjectGlobal--Release.md)|Implements a global **Release**.|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CComObjectGlobal::m_hResFinalConstruct](../vs140/CComObjectGlobal--m_hResFinalConstruct.md)|Contains the  **HRESULT** returned during construction of the `CComObjectGlobal` object.|  
  
## Remarks  
 `CComObjectGlobal` manages a reference count on the module containing your `Base` object. `CComObjectGlobal` ensures your object will not be deleted as long as the module is not released. Your object will only be removed when the reference count on the entire module goes to zero.  
  
 For example, using `CComObjectGlobal`, a class factory can hold a common global object that is shared by all its clients.  
  
## Inheritance Hierarchy  
 `Base`  
  
 `CComObjectGlobal`  
  
## Requirements  
 **Header:** atlcom.h  
  
##  <a name="ccomobjectglobal__addref"></a>  CComObjectGlobal::AddRef  
 Increments the reference count of the object by 1.  
  
```  
  
STDMETHOD_(ULONG, AddRef)( );  
  
```  
  
### Return Value  
 A value that may be useful for diagnostics and testing.  
  
### Remarks  
 By default, `AddRef` calls **_Module::Lock**, where **_Module** is the global instance of [CComModule](../vs140/CComModule-Class.md) or a class derived from it.  
  
##  <a name="ccomobjectglobal__ccomobjectglobal"></a>  CComObjectGlobal::CComObjectGlobal  
 The constructor. Calls `FinalConstruct` and then sets [m_hResFinalConstruct](../vs140/CComObjectGlobal--m_hResFinalConstruct.md) to the `HRESULT` returned by `FinalConstruct`.  
  
```  
  
CComObjectGlobal(   
      void* = NULL   
   )  
   );  
  
```  
  
### Remarks  
 If you have not derived your base class from [CComObjectRoot](../vs140/CComObjectRoot-Class.md), you must supply your own `FinalConstruct` method. The destructor calls `FinalRelease`.  
  
##  <a name="ccomobjectglobal___dtorccomobjectglobal"></a>  CComObjectGlobal::~CComObjectGlobal  
 The destructor.  
  
```  
  
CComObjectGlobal( );  
  
```  
  
### Remarks  
 Frees all allocated resources and calls [FinalRelease](../vs140/CComObjectRootEx--FinalRelease.md).  
  
##  <a name="ccomobjectglobal__m_hresfinalconstruct"></a>  CComObjectGlobal::m_hResFinalConstruct  
 Contains the `HRESULT` from calling `FinalConstruct` during construction of the `CComObjectGlobal` object.  
  
```  
  
HRESULT  
   m_hResFinalConstruct;  
  
```  
  
##  <a name="ccomobjectglobal__queryinterface"></a>  CComObjectGlobal::QueryInterface  
 Retrieves a pointer to the requested interface pointer.  
  
```  
  
STDMETHOD(QueryInterface)(  
      REFIID iid,  
   void** ppvObject  
   )  
   ;  
  
```  
  
### Parameters  
 `iid`  
 [in] The GUID of the interface being requested.  
  
 `ppvObject`  
 [out] A pointer to the interface pointer identified by iid, or **NULL** if the interface is not found.  
  
### Return Value  
 A standard `HRESULT` value.  
  
### Remarks  
 `QueryInterface` only handles interfaces in the COM map table.  
  
##  <a name="ccomobjectglobal__release"></a>  CComObjectGlobal::Release  
 Decrements the reference count of the object by 1.  
  
```  
  
STDMETHOD_(ULONG, Release)(  
   );  
  
```  
  
### Return Value  
 In debug builds,                         **Release** returns a value that may be useful for diagnostics and testing. In non-debug builds,                         **Release** always returns 0.  
  
### Remarks  
 By default,                         **Release** calls **_Module::Unlock**, where **_Module** is the global instance of [CComModule](../vs140/CComModule-Class.md) or a class derived from it.  
  
## See Also  
 [CComObjectStack Class](../vs140/CComObjectStack-Class.md)   
 [CComAggObject Class](../vs140/CComAggObject-Class.md)   
 [CComObject Class](../vs140/CComObject-Class.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)