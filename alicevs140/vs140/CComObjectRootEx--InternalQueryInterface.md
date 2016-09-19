---
title: "CComObjectRootEx::InternalQueryInterface"
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
ms.assetid: 0d90c9b1-ebf9-4e70-8513-aa96e366879a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComObjectRootEx::InternalQueryInterface
Retrieves a pointer to the requested interface.  
  
## Syntax  
  
```  
  
      static HRESULT InternalQueryInterface(  
   void* pThis,  
   const _ATL_INTMAP_ENTRY* pEntries,  
   REFIID iid,  
   void** ppvObject   
);  
```  
  
#### Parameters  
 `pThis`  
 [in] A pointer to the object that contains the COM map of interfaces exposed to `QueryInterface`.  
  
 `pEntries`  
 [in] A pointer to the **_ATL_INTMAP_ENTRY** structure that accesses a map of available interfaces.  
  
 `iid`  
 [in] The GUID of the interface being requested.  
  
 `ppvObject`  
 [out] A pointer to the interface pointer specified in `iid`, or **NULL** if the interface is not found.  
  
## Return Value  
 One of the standard `HRESULT` values.  
  
## Remarks  
 `InternalQueryInterface` only handles interfaces in the COM map table. If your object is aggregated, `InternalQueryInterface` does not delegate to the outer unknown. You can enter interfaces into the COM map table with the macro [COM_INTERFACE_ENTRY](../vs140/COM_INTERFACE_ENTRY-Macros.md) or one of its variants.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComObjectRootEx Class](../vs140/CComObjectRootEx-Class.md)   
 [CComObjectRootEx::InternalAddRef](../vs140/CComObjectRootEx--InternalAddRef.md)   
 [CComObjectRootEx::InternalRelease](../vs140/CComObjectRootEx--InternalRelease.md)