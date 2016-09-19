---
title: "CComObjectStack Class"
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
ms.assetid: 3da72c40-c834-45f6-bb76-6ac204028d80
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComObjectStack Class
This class creates a temporary COM object and provides it with a skeletal implementation of             **IUnknown**.  
  
## Syntax  
  
```  
  
template<  
   class   
Base  
>  
class  
CComObjectStack  
:  
public  
Base  
  
```  
  
#### Parameters  
 `Base`  
 Your class, derived from                         [CComObjectRoot](../vs140/CComObjectRoot-Class.md) or                         [CComObjectRootEx](../vs140/CComObjectRootEx-Class.md), as well as from any other interface you want to support on the object.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CComObjectStack::CComObjectStack](../vs140/CComObjectStack--CComObjectStack.md)|The constructor.|  
|[CComObjectStack::~CComObjectStack](../vs140/CComObjectStack--~CComObjectStack.md)|The destructor.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CComObjectStack::AddRef](../vs140/CComObjectStack--AddRef.md)|Returns zero. In debug mode, calls                                         `_ASSERTE`.|  
|[CComObjectStack::QueryInterface](../vs140/CComObjectStack--QueryInterface.md)|Returns                                         **E_NOINTERFACE**. In debug mode, calls                                         `_ASSERTE`.|  
|[CComObjectStack::Release](../vs140/CComObjectStack--Release.md)|Returns zero. In debug mode, calls                                         `_ASSERTE`. ~|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CComObjectStack::m_hResFinalConstruct](../vs140/CComObjectStack--m_hResFinalConstruct.md)|Contains the                                         **HRESULT** returned during construction of the                                         `CComObjectStack` object.|  
  
## Remarks  
 `CComObjectStack` is used to create a temporary COM object and provide the object a skeletal implementation of                 **IUnknown**. Typically, the object is used as a local variable within one function (that is, pushed onto the stack). Since the object is destroyed when the function finishes, reference counting is not performed to increase efficiency.  
  
 The following example shows how to create a COM object used inside a function:  
  
 [!CODE [NVC_ATL_COM#42](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#42)]  
  
 The temporary object                 `Tempobj` is pushed onto the stack and automatically disappears when the function finishes.  
  
## Inheritance Hierarchy  
 `Base`  
  
 `CComObjectStack`  
  
## Requirements  
 **Header:** atlcom.h  
  
##  <a name="ccomobjectstack__addref"></a>  CComObjectStack::AddRef  
 Returns zero.  
  
```  
  
STDMETHOD_(ULONG, AddRef)( );  
  
```  
  
### Return Value  
 Returns zero.  
  
### Remarks  
 In debug mode, calls                         `_ASSERTE`.  
  
##  <a name="ccomobjectstack__ccomobjectstack"></a>  CComObjectStack::CComObjectStack  
 The constructor.  
  
```  
  
CComObjectStack(  
   void* = NULL   
);  
  
```  
  
### Remarks  
 Calls                         `FinalConstruct` and then sets                         [m_hResFinalConstruct](../vs140/CComObjectStack--m_hResFinalConstruct.md) to the                         `HRESULT` returned by                         `FinalConstruct`. If you have not derived your base class from                         [CComObjectRoot](../vs140/CComObjectRoot-Class.md), you must supply your own                         `FinalConstruct` method. The destructor calls                         `FinalRelease`.  
  
##  <a name="ccomobjectstack___dtorccomobjectstack"></a>  CComObjectStack::~CComObjectStack  
 The destructor.  
  
```  
  
CComObjectStack( );  
  
```  
  
### Remarks  
 Frees all allocated resources and calls                         [FinalRelease](../vs140/CComObjectRootEx--FinalRelease.md).  
  
##  <a name="ccomobjectstack__m_hresfinalconstruct"></a>  CComObjectStack::m_hResFinalConstruct  
 Contains the                 `HRESULT` returned from calling                 `FinalConstruct` during construction of the                 `CComObjectStack` object.  
  
```  
  
HRESULT  
m_hResFinalConstruct;  
  
```  
  
##  <a name="ccomobjectstack__queryinterface"></a>  CComObjectStack::QueryInterface  
 Returns                 **E_NOINTERFACE**.  
  
```  
  
HRESULT  
QueryInterface(  
   REFIID,  
   void**  
)  
;  
  
```  
  
### Return Value  
 Returns                         **E_NOINTERFACE**.  
  
### Remarks  
 In debug mode, calls                         `_ASSERTE`.  
  
##  <a name="ccomobjectstack__release"></a>  CComObjectStack::Release  
 Returns zero.  
  
```  
  
STDMETHOD_(ULONG, Release)( );  
  
```  
  
### Return Value  
 Returns zero.  
  
### Remarks  
 In debug mode, calls                         `_ASSERTE`.  
  
## See Also  
 [CComAggObject Class](../vs140/CComAggObject-Class.md)   
 [CComObject Class](../vs140/CComObject-Class.md)   
 [CComObjectGlobal Class](../vs140/CComObjectGlobal-Class.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)