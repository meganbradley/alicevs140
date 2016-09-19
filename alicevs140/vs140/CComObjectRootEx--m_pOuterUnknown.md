---
title: "CComObjectRootEx::m_pOuterUnknown"
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
ms.assetid: 3b924765-e280-44dc-87a3-937864d0060c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComObjectRootEx::m_pOuterUnknown
Part of a union that accesses four bytes of memory.  
  
## Syntax  
  
```  
  
IUnknown* m_pOuterUnknown;  
```  
  
## Remarks  
 With `m_dwRef`, part of a union:  
  
 `union`  
  
 `{`  
  
 `long m_dwRef;`  
  
 `IUnknown* m_pOuterUnknown;`  
  
 `};`  
  
 If the object is aggregated, the pointer to the outer unknown is stored in `m_pOuterUnknown`. If the object is not aggregated, the reference count accessed by `AddRef` and **Release** is stored in [m_dwRef](../vs140/CComObjectRootEx--m_dwRef.md).  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComObjectRootEx Class](../vs140/CComObjectRootEx-Class.md)