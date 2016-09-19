---
title: "CComCachedTearOffObject::CComCachedTearOffObject"
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
ms.assetid: ee80eb8e-7983-4d48-bd33-b097cb232265
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComCachedTearOffObject::CComCachedTearOffObject
The constructor.  
  
## Syntax  
  
```  
  
      CComCachedTearOffObject(  
   void* pv   
);  
```  
  
#### Parameters  
 `pv`  
 [in] Pointer to the **IUnknown** of the `CComCachedTearOffObject`.  
  
## Remarks  
 Initializes the `CComContainedObject` member, [m_contained](../vs140/CComCachedTearOffObject--m_contained.md).  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComCachedTearOffObject Class](../vs140/CComCachedTearOffObject-Class.md)   
 [CComTearOffObject Class](../vs140/CComTearOffObject-Class.md)