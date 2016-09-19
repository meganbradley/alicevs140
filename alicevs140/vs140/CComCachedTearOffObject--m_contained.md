---
title: "CComCachedTearOffObject::m_contained"
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
ms.assetid: 425023b3-c2f8-4cc3-ae10-9a26f169a636
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComCachedTearOffObject::m_contained
A [CComContainedObject](../vs140/CComContainedObject-Class.md) object derived from your tear-off class.  
  
## Syntax  
  
```  
  
CcomContainedObject <  
contained  
> m_contained;  
```  
  
#### Parameters  
 `contained`  
 [in] Your tear-off class, derived from `CComTearOffObjectBase` and the interfaces you want your tear-off object to support.  
  
## Remarks  
 The methods `m_contained` inherits are used to access the tear-off interface in your tear-off class through the cached tear-off object's `QueryInterface`, `FinalConstruct`, and `FinalRelease`.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComCachedTearOffObject Class](../vs140/CComCachedTearOffObject-Class.md)   
 [CComTearOffObject Class](../vs140/CComTearOffObject-Class.md)