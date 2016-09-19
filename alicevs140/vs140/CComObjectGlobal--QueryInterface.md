---
title: "CComObjectGlobal::QueryInterface"
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
ms.assetid: 66122a8a-2bdb-4436-b40a-12708db5b53c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComObjectGlobal::QueryInterface
Retrieves a pointer to the requested interface pointer.  
  
## Syntax  
  
```  
  
      STDMETHOD(QueryInterface)(  
   REFIID iid,  
   void** ppvObject   
) ;  
```  
  
#### Parameters  
 `iid`  
 [in] The GUID of the interface being requested.  
  
 `ppvObject`  
 [out] A pointer to the interface pointer identified by iid, or **NULL** if the interface is not found.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
 `QueryInterface` only handles interfaces in the COM map table.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComObjectGlobal Class](../vs140/CComObjectGlobal-Class.md)   
 [CComObjectRootEx::InternalQueryInterface](../vs140/CComObjectRootEx--InternalQueryInterface.md)   
 [BEGIN_COM_MAP](../vs140/BEGIN_COM_MAP.md)