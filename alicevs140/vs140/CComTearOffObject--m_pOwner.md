---
title: "CComTearOffObject::m_pOwner"
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
ms.assetid: ef2e3985-d279-4394-8d73-7927f8a244d8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComTearOffObject::m_pOwner
A pointer to a [CComObject](../vs140/CComObject-Class.md) object derived from *Owner*.  
  
## Syntax  
  
```  
  
CComObject<  
Owner  
>* m_pOwner;  
  
```  
  
#### Parameters  
 *Owner*  
 [in] The class for which a tear-off is being implemented.  
  
## Remarks  
 The pointer is initialized to **NULL** during construction.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComTearOffObject Class](../vs140/CComTearOffObject-Class.md)   
 [CComTearOffObject::CComTearOffObjectBase](../vs140/CComTearOffObject--CComTearOffObjectBase.md)