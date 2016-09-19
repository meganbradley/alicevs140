---
title: "CComAggObject::m_contained"
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
ms.assetid: fc4bef4b-d0b8-4034-abb9-00e50bf6a33c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComAggObject::m_contained
A [CComContainedObject](../vs140/CComContainedObject-Class.md) object derived from your class.  
  
## Syntax  
  
```  
  
CComContainedObject<   
contained  
 > m_contained;  
  
```  
  
#### Parameters  
 `contained`  
 [in] Your class, derived from [CComObjectRoot](../vs140/CComObjectRoot-Class.md) or [CComObjectRootEx](../vs140/CComObjectRootEx-Class.md), as well as from any other interfaces you want to support on the object.  
  
## Remarks  
 All **IUnknown** calls through `m_contained` are delegated to the outer unknown.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComAggObject Class](../vs140/CComAggObject-Class.md)