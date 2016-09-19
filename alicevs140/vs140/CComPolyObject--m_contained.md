---
title: "CComPolyObject::m_contained"
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
ms.assetid: 13cae859-302f-4e6d-8931-ec7f12e0c42f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComPolyObject::m_contained
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
 **IUnknown** calls through `m_contained` are delegated to the outer unknown if the object is aggregated, or to the **IUnknown** of this object if the object is not aggregated.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComPolyObject Class](../vs140/CComPolyObject-Class.md)