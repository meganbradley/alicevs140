---
title: "CHandle Class"
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
ms.assetid: 883e9db5-40ec-4e29-9c74-4dd2ddd2e35d
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHandle Class
This class provides methods for creating and using a handle object.  
  
## Syntax  
  
```  
  
class CHandle  
  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CHandle::CHandle](../vs140/CHandle--CHandle.md)|The constructor.|  
|[CHandle::~CHandle](../vs140/CHandle--~CHandle.md)|The destructor.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CHandle::Attach](../vs140/CHandle--Attach.md)|Call this method to attach the `CHandle` object to an existing handle.|  
|[CHandle::Close](../vs140/CHandle--Close.md)|Call this method to close a `CHandle` object.|  
|[CHandle::Detach](../vs140/CHandle--Detach.md)|Call this method to detach a handle from a `CHandle` object.|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[CHandle::operator HANDLE](../vs140/CHandle--operator-HANDLE.md)|Returns the value of the stored handle.|  
|[CHandle::operator =](../vs140/CHandle--operator-=.md)|Assignment operator.|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CHandle::m_h](../vs140/CHandle--m_h.md)|The member variable that stores the handle.|  
  
## Remarks  
 A `CHandle` object can be used whenever a handle is required: the main difference is that the `CHandle` object will automatically be deleted.  
  
> [!NOTE]
>  Some API functions will use NULL as an empty or invalid handle, while others use INVALID_HANDLE_VALUE. `CHandle` only uses NULL and will treat INVALID_HANDLE_VALUE as a real handle. If you call an API which can return INVALID_HANDLE_VALUE, you should check for this value before calling [CHandle::Attach](../vs140/CHandle--Attach.md) or passing it to the `CHandle` constructor, and instead pass NULL.  
  
## Requirements  
 **Header:** atlbase.h  
  
##  <a name="chandle__attach"></a>  CHandle::Attach  
 Call this method to attach the `CHandle` object to an existing handle.  
  
```  
  
void Attach(  
      HANDLE  h  
   ) throw( );  
  
```  
  
### Parameters  
 `h`  
 `CHandle` will take ownership of the handle `h`.  
  
### Remarks  
 Assigns the `CHandle` object to the `h` handle. In debugs builds, an ATLASSERT will be raised if `h` is NULL. No other check as to the validity of the handle is made.  
  
##  <a name="chandle__chandle"></a>  CHandle::CHandle  
 The constructor.  
  
```  
  
CHandle( ) throw( );   
   CHandle(  
      CHandle&  h  
   ) throw( );  
   explicit CHandle(  
      HANDLE  h  
   ) throw( );  
  
```  
  
### Parameters  
 `h`  
 An existing handle or `CHandle`.  
  
### Remarks  
 Creates a new `CHandle` object, optionally using an existing handle or `CHandle` object.  
  
##  <a name="chandle___dtorchandle"></a>  CHandle::~CHandle  
 The destructor.  
  
```  
  
~CHandle( ) throw( );  
  
```  
  
### Remarks  
 Frees the `CHandle` object by calling [CHandle::Close](../vs140/CHandle--Close.md).  
  
##  <a name="chandle__close"></a>  CHandle::Close  
 Call this method to close a `CHandle` object.  
  
```  
  
void Close( ) throw( );  
  
```  
  
### Remarks  
 Closes an open object handle. If the handle is NULL, which will be the case if **Close** has already been called, an ATLASSERT will be raised in debug builds.  
  
##  <a name="chandle__detach"></a>  CHandle::Detach  
 Call this method to detach a handle from a `CHandle` object.  
  
```  
  
HANDLE Detach( ) throw( );  
  
```  
  
### Return Value  
 Returns the handle being detached.  
  
### Remarks  
 Releases ownership of the handle.  
  
##  <a name="chandle__m_h"></a>  CHandle::m_h  
 The member variable that stores the handle.  
  
```  
  
HANDLE m_h;  
  
```  
  
##  <a name="chandle__operator__eq"></a>  CHandle::operator =  
 The assignment operator.  
  
```  
  
CHandle& operator =(   
      CHandle&  h    
   ) throw( );  
  
```  
  
### Parameters  
 `h`  
 `CHandle` will take ownership of the handle `h`.  
  
### Return Value  
 Returns a reference to the new `CHandle` object.  
  
### Remarks  
 If the `CHandle` object currently contains a handle, it will be closed. The `CHandle` object being passed in will have its handle reference set to NULL. This ensures that two `CHandle` objects will never contain the same active handle.  
  
##  <a name="chandle__operator_handle"></a>  CHandle::operator HANDLE  
 Returns the value of the stored handle.  
  
```  
  
operator HANDLE( ) const throw( );  
  
```  
  
### Remarks  
 Returns the value stored in [CHandle::m_h](../vs140/CHandle--m_h.md).  
  
## See Also  
 [Class Overview](../vs140/ATL-Class-Overview.md)