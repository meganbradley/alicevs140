---
title: "CComCachedTearOffObject::QueryInterface"
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
ms.assetid: d44db5f6-305a-4ae5-a5bc-c0286d743b36
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComCachedTearOffObject::QueryInterface
Retrieves a pointer to the requested interface.  
  
## Syntax  
  
```  
  
      STDMETHOD(QueryInterface)(  
   REFIID iid ,  
   void** ppvObject   
);  
```  
  
#### Parameters  
 `iid`  
 [in] The GUID of the interface being requested.  
  
 `ppvObject`  
 [out] A pointer to the interface pointer identified by `iid`, or **NULL** if the interface is not found.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
 If the requested interface is **IUnknown**, returns a pointer to the `CComCachedTearOffObject`'s own **IUnknown** and increments the reference count. Otherwise, queries for the interface on your tear-off class using the [InternalQueryInterface](../vs140/CComObjectRootEx--InternalQueryInterface.md) method inherited from `CComObjectRootEx`.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComCachedTearOffObject Class](../vs140/CComCachedTearOffObject-Class.md)   
 [CComCachedTearOffObject::AddRef](../vs140/CComCachedTearOffObject--AddRef.md)   
 [CComCachedTearOffObject::Release](../vs140/CComCachedTearOffObject--Release.md)