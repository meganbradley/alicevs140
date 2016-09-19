---
title: "CComObjectNoLock Class"
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
ms.assetid: 288c6506-7da8-4127-8d58-7f4bd779539a
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComObjectNoLock Class
This class implements **IUnknown** for a nonaggregated object, but does not increment the module lock count in the constructor.  
  
## Syntax  
  
```  
  
template<  
      class  Base>  
   class CComObjectNoLock :  
      public  Base  
  
```  
  
#### Parameters  
 `Base`  
 Your class, derived from [CComObjectRoot](../vs140/CComObjectRoot-Class.md) or [CComObjectRootEx](../vs140/CComObjectRootEx-Class.md), as well as from any other interface you want to support on the object.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CComObjectNoLock::CComObjectNoLock](../vs140/CComObjectNoLock--CComObjectNoLock.md)|Constructor.|  
|[CComObjectNoLock::~CComObjectNoLock](../vs140/CComObjectNoLock--~CComObjectNoLock.md)|The destructor.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CComObjectNoLock::AddRef](../vs140/CComObjectNoLock--AddRef.md)|Increments the reference count on the object.|  
|[CComObjectNoLock::QueryInterface](../vs140/CComObjectNoLock--QueryInterface.md)|Returns a pointer to the requested interface.|  
|[CComObjectNoLock::Release](../vs140/CComObjectNoLock--Release.md)|Decrements the reference count on the object.|  
  
## Remarks  
 `CComObjectNoLock` is similar to [CComObject](../vs140/CComObject-Class.md) in that it implements [IUnknown](http://msdn.microsoft.com/library/windows/desktop/ms680509) for a nonaggregated object; however, `CComObjectNoLock` does not increment the module lock count in the constructor.  
  
 ATL uses `CComObjectNoLock` internally for class factories. In general, you will not use this class directly.  
  
## Inheritance Hierarchy  
 `Base`  
  
 `CComObjectNoLock`  
  
## Requirements  
 **Header:** atlcom.h  
  
##  <a name="ccomobjectnolock__addref"></a>  CComObjectNoLock::AddRef  
 Increments the reference count on the object.  
  
```  
  
STDMETHOD_(ULONG, AddRef)( );  
  
```  
  
### Return Value  
 A value that may be useful for diagnostics or testing.  
  
##  <a name="ccomobjectnolock__ccomobjectnolock"></a>  CComObjectNoLock::CComObjectNoLock  
 The constructor. Unlike [CComObject](../vs140/CComObject-Class.md), does not increment the module lock count.  
  
```  
  
CComObjectNoLock(  
      void* = NULL   
   );  
  
```  
  
### Parameters  
 **void\***  
 [in] This unnamed parameter is not used. It exists for symmetry with other **CCom***XXX*`Object`*XXX* constructors.  
  
##  <a name="ccomobjectnolock___dtorccomobjectnolock"></a>  CComObjectNoLock::~CComObjectNoLock  
 The destructor.  
  
```  
  
~CComObjectNoLock( );  
  
```  
  
### Remarks  
 Frees all allocated resources and calls [FinalRelease](../vs140/CComObjectRootEx--FinalRelease.md).  
  
##  <a name="ccomobjectnolock__queryinterface"></a>  CComObjectNoLock::QueryInterface  
 Retrieves a pointer to the requested interface.  
  
```  
  
STDMETHOD(QueryInterface)(  
      REFIID  iid,  
      void**  ppvObject  
   );  
  
```  
  
### Parameters  
 `iid`  
 [in] The identifier of the interface being requested.  
  
 `ppvObject`  
 [out] A pointer to the interface pointer identified by `iid`. If the object does not support this interface, `ppvObject` is set to **NULL**.  
  
### Return Value  
 A standard `HRESULT` value.  
  
##  <a name="ccomobjectnolock__release"></a>  CComObjectNoLock::Release  
 Decrements the reference count on the object.  
  
```  
  
STDMETHOD_(ULONG, Release)( );  
  
```  
  
### Return Value  
 In debug builds,                         **Release** returns a value that may be useful for diagnostics or testing. In non-debug builds,                         **Release** always returns 0.  
  
## See Also  
 [Class Overview](../vs140/ATL-Class-Overview.md)