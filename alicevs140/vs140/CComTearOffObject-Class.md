---
title: "CComTearOffObject Class"
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
ms.assetid: d974b598-c6b2-42b1-8360-9190d9d0fbf3
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComTearOffObject Class
This class implements a tear-off interface.  
  
## Syntax  
  
```  
  
template<  
      class Base>  
   class  
   CComTearOffObject  
   :  
   public Base  
  
```  
  
#### Parameters  
 `Base`  
 Your tear-off class, derived from `CComTearOffObjectBase` and the interfaces you want your tear-off object to support.  
  
 ATL implements its tear-off interfaces in two phases — the `CComTearOffObjectBase` methods handle the reference count and `QueryInterface`, while `CComTearOffObject` implements [IUnknown](http://msdn.microsoft.com/library/windows/desktop/ms680509).  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CComTearOffObject::CComTearOffObject](../vs140/CComTearOffObject--CComTearOffObject.md)|The constructor.|  
|[CComTearOffObject::~CComTearOffObject](../vs140/CComTearOffObject--~CComTearOffObject.md)|The destructor.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CComTearOffObject::AddRef](../vs140/CComTearOffObject--AddRef.md)|Increments the reference count for a `CComTearOffObject` object.|  
|[CComTearOffObject::QueryInterface](../vs140/CComTearOffObject--QueryInterface.md)|Returns a pointer to the requested interface on either your tear-off class or the owner class.|  
|[CComTearOffObject::Release](../vs140/CComTearOffObject--Release.md)|Decrements the reference count for a `CComTearOffObject` object and destroys it.|  
  
### CComTearOffObjectBase Methods  
  
|||  
|-|-|  
|[CComTearOffObjectBase](../vs140/CComTearOffObject--CComTearOffObjectBase.md)|Constructor.|  
  
### CComTearOffObjectBase Data Members  
  
|||  
|-|-|  
|[m_pOwner](../vs140/CComTearOffObject--m_pOwner.md)|A pointer to a `CComObject` derived from the owner class.|  
  
## Remarks  
 `CComTearOffObject` implements a tear-off interface as a separate object that is instantiated only when that interface is queried for. The tear-off is deleted when its reference count becomes zero. Typically, you build a tear-off interface for an interface that is rarely used, since using a tear-off saves a vtable pointer in all the instances of your main object.  
  
 You should derive the class implementing the tear-off from `CComTearOffObjectBase` and from whichever interfaces you want your tear-off object to support. `CComTearOffObjectBase` is templatized on the owner class and the thread model. The owner class is the class of the object for which a tear-off is being implemented. If you do not specify a thread model, the default thread model is used.  
  
 You should create a COM map for your tear-off class. When ATL instantiates the tear-off, it will create **CComTearOffObject<CYourTearOffClass\>** or **CComCachedTearOffObject<CYourTearOffClass\>**.  
  
 For example, in the BEEPER sample, the `CBeeper2` class is the tear-off class and the `CBeeper` class is the owner class:  
  
 [!CODE [NVC_ATL_COM#43](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#43)]  
  
## Inheritance Hierarchy  
 `Base`  
  
 `CComTearOffObject`  
  
## Requirements  
 **Header:** atlcom.h  
  
##  <a name="ccomtearoffobject__addref"></a>  CComTearOffObject::AddRef  
 Increments the reference count of the `CComTearOffObject` object by one.  
  
```  
  
STDMETHOD_(ULONG, AddRef)( );  
  
```  
  
### Return Value  
 A value that may be useful for diagnostics and testing.  
  
##  <a name="ccomtearoffobject__ccomtearoffobject"></a>  CComTearOffObject::CComTearOffObject  
 The constructor.  
  
```  
  
CComTearOffObject(  
      void* pv  
   );  
  
```  
  
### Parameters  
 `pv`  
 [in] Pointer that will be converted to a pointer to a **CComObject<Owner\>** object.  
  
### Remarks  
 Increments the owner's reference count by one.  
  
##  <a name="ccomtearoffobject___dtorccomtearoffobject"></a>  CComTearOffObject::~CComTearOffObject  
 The destructor.  
  
```  
  
~CComTearOffObject( );  
  
```  
  
### Remarks  
 Frees all allocated resources, calls FinalRelease, and decrements the module lock count.  
  
##  <a name="ccomtearoffobject__ccomtearoffobjectbase"></a>  CComTearOffObject::CComTearOffObjectBase  
 The constructor.  
  
```  
  
CComTearOffObjectBase(  
   );  
  
```  
  
### Remarks  
 Initializes the [m_pOwner](../vs140/CComTearOffObject--m_pOwner.md) member to **NULL**.  
  
##  <a name="ccomtearoffobject__m_powner"></a>  CComTearOffObject::m_pOwner  
 A pointer to a [CComObject](../vs140/CComObject-Class.md) object derived from *Owner*.  
  
```  
  
CComObject< Owner  
   >* m_pOwner;  
  
```  
  
### Parameters  
 *Owner*  
 [in] The class for which a tear-off is being implemented.  
  
### Remarks  
 The pointer is initialized to  **NULL** during construction.  
  
##  <a name="ccomtearoffobject__queryinterface"></a>  CComTearOffObject::QueryInterface  
 Retrieves a pointer to the requested interface.  
  
```  
  
STDMETHOD(QueryInterface)(  
      REFIID iid ,  
   void** ppvObject  
   );  
  
```  
  
### Parameters  
 `iid`  
 [in] The IID of the interface being requested.  
  
 `ppvObject`  
 [out] A pointer to the interface pointer identified by `iid`, or **NULL** if the interface is not found.  
  
### Return Value  
 A standard `HRESULT` value.  
  
### Remarks  
 Queries first for interfaces on your tear-off class. If the interface is not there, queries for the interface on the owner object. If the requested interface is **IUnknown**, returns the **IUnknown** of the owner.  
  
##  <a name="ccomtearoffobject__release"></a>  CComTearOffObject::Release  
 Decrements the reference count by one and, if the reference count is zero, deletes the `CComTearOffObject`.  
  
```  
  
STDMETHOD_ULONG  
   Release(  
   );  
  
```  
  
### Return Value  
 In non-debug builds, always returns zero. In debug builds, returns a value that may be useful for diagnostics or testing.  
  
## See Also  
 [CComCachedTearOffObject Class](../vs140/CComCachedTearOffObject-Class.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)