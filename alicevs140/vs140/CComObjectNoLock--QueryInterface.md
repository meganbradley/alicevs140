---
title: "CComObjectNoLock::QueryInterface"
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
ms.assetid: ffffe7ca-9d3a-41da-b594-d30a6e090701
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComObjectNoLock::QueryInterface
Retrieves a pointer to the requested interface.  
  
## Syntax  
  
```  
  
      STDMETHOD(QueryInterface)(  
   REFIID iid,  
   void** ppvObject   
);  
```  
  
#### Parameters  
 `iid`  
 [in] The identifier of the interface being requested.  
  
 `ppvObject`  
 [out] A pointer to the interface pointer identified by `iid`. If the object does not support this interface, `ppvObject` is set to **NULL**.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComObjectNoLock Class](../vs140/CComObjectNoLock-Class.md)