---
title: "CComTearOffObject::CComTearOffObject"
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
ms.assetid: 443f94dc-bc5c-4e9f-a45e-19ebec3bfcf4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComTearOffObject::CComTearOffObject
The constructor.  
  
## Syntax  
  
```  
  
      CComTearOffObject(  
   void* pv   
);  
```  
  
#### Parameters  
 `pv`  
 [in] Pointer that will be converted to a pointer to a **CComObject<Owner\>** object.  
  
## Remarks  
 Increments the owner's reference count by one.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComTearOffObject Class](../vs140/CComTearOffObject-Class.md)   
 [CComCachedTearOffObject::CComCachedTearOffObject](../vs140/CComCachedTearOffObject--CComCachedTearOffObject.md)